<template>
	<div>
		<div class="news-popup-top">
			<div
				class="news-popup-top__tags news-tags"
				v-for="tagName in tagsNames"
				:key="tagName"
			>
				<div class="news-tags__item">
					<span>{{ tagName[0] }}</span>
				</div>
				<div class="news-tags__item">
					<!-- <img src="/public/images/icons/percent-icon.svg" alt="icon" /> -->
					<span>{{ tagName[1] }}</span>
				</div>
			</div>
			<h1 class="news-popup-top__title">
				{{ title }}
			</h1>
			<div class="news-popup-top__date">06.10.2023</div>
		</div>
	</div>
</template>

<script setup>
const props = defineProps({
	title: { type: String },
	tagsNames: { type: Array },
	tagsColors: { type: Array },
});
// console.log(props.tagsNames);
</script>

<style lang="scss" scoped></style>
