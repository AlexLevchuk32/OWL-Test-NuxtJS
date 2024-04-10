<template>
	<div>
		<div class="news-popup-content">
			<p class="news-popup-content__text" v-for="text in textContent" :key="text">
				{{ text }}
			</p>
			<img
				class="news-popup-content__img"
				src="/public/images/news-photo/playground.webp"
				alt="playground"
			/>
		</div>
	</div>
</template>

<script setup>
const props = defineProps({
	textContent: { type: Array },
});
</script>

<style lang="scss" scoped></style>
