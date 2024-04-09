<template>
	<div>
		<div class="news-popup-top">
			<div
				class="news-popup-top__tags news-tags"
				v-for="(tagName, index) in tagsNames"
				:key="tagName"
			>
				<template v-for="(color, index) in tagsColors" :key="color">
					<div :class="'news-tags__item--' + color[index]">
						<span>{{ tagName[index] }}</span>
					</div>
					<div :class="'news-tags__item--' + color[index + 1]">
						<!-- <img src="/public/images/icons/percent-icon.svg" alt="icon" /> -->
						<span>{{ tagName[index + 1] }}</span>
					</div>
				</template>
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
