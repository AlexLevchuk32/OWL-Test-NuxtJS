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
					:tagsNames="[tagsNames()]"
					:tagsColors="[tagsColors()]"
				/>

				<NewsPopupPageContent :textContent="textContent()" />

				<NewsPopupPageCardNext
					:nextTitle="nextTitle"
					:nextTagsNames="[nextTagsNames()]"
					:nextTagsColors="[nextTagsColors()]"
					:nextPicture="nextPicture"
				/>
			</div>
		</section>
	</div>
</template>

<script setup>
const title = ref();
const tags = ref();
const text = ref();
const tagsNames = ref();
const tagsColors = ref();
const textContent = ref();
const nextTitle = ref();
const nextTags = ref();
const nextTagsNames = ref();
const nextTagsColors = ref();
const nextPicture = ref();

const { data } = await useFetch(
	'https://bsk-admin-test.testers-site.ru/api/news/novogodnee-vesele-ot-kompanii-bsk-kak-proshla-yelkabsk-v-2023-godu',
);
// console.log(data);

title._value = data._value.data.result.title;
tags._value = data._value.data.result.tags;
text._value = data._value.data.result.content;
nextTitle._value = data._value.data.result.next.title;
nextTags._value = data._value.data.result.next.tags;
nextPicture._value = data._value.data.result.next.picture;

// console.log(title._value);
// console.log(tags._value);
// console.log(tags._value[0].values[0].name);
// console.log(data._value.data.result.tags[0]);
// console.log(text._value);
console.log(nextPicture._value);

//=========================================================================================================================================================
// Top
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

//=========================================================================================================================================================
// Content
textContent._value = () => {
	const textsArr = [];

	text._value.forEach((el) => {
		if (el.hasOwnProperty('content')) {
			textsArr.push(el.content);
		}
	});

	return textsArr;
};
// console.log(textContent._value());

//=========================================================================================================================================================
// CardNext
nextTagsNames._value = () => {
	const nextNamesArr = [];

	nextTags._value.forEach((el) => {
		nextNamesArr.push(el.values[0].name);
	});

	return nextNamesArr;
};
// console.log(tagsNames._value());

nextTagsColors._value = () => {
	const nextColorsArr = [];

	nextTags._value.forEach((el) => {
		nextColorsArr.push(el.values[0].color);
	});

	return nextColorsArr;
};
</script>

<style lang="scss" scoped></style>
