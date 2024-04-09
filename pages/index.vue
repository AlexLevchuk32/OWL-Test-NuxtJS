<template>
	<div>
		<section class="news-popup">
			<div class="container">
				<NewsPopupPageCloseBtn />

				<div class="news-popup__header">
					<NewsPopupPageBreadcrumbs />
				</div>

				<NewsPopupPageTop
					:title="title"
					:tagsNames="[tagsNames]"
					:tagsColors="[tagsColors]"
				/>

				<NewsPopupPageContent />

				<NewsPopupPageCardNext />
			</div>
		</section>
	</div>
</template>

<script setup>
const title = ref();
const tags = ref();
const tagsNames = ref();
const tagsColors = ref();

const { data } = await useFetch(
	'https://bsk-admin-test.testers-site.ru/api/news/novogodnee-vesele-ot-kompanii-bsk-kak-proshla-yelkabsk-v-2023-godu',
	{},
);

// console.log(data._value.data.result.tags[0]);

title._value = data._value.data.result.title;
tags._value = data._value.data.result.tags;

// console.log(title._value);
// console.log(tags._values);
// console.log(tags._value[0].values[0].name);

tagsNames._value = () => {
	const namesArr = [];

	tags._value.forEach((el) => {
		namesArr.push(el.values[0].name);
	});

	return namesArr;
};
// console.log(tagsNames._value());

tagsColors._value = () => {
	const colorsArr = [];

	tags._value.forEach((el) => {
		colorsArr.push(el.values[0].color);
	});

	return colorsArr;
};
// console.log(tagsColors._value());
</script>

<style lang="scss" scoped></style>
