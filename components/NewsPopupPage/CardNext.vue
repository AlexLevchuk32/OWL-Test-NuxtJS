<template>
	<div>
		<div class="news-popup__next news-card">
			<h2 class="news-card__title">Следующая статья</h2>
			<a href="#" class="news-card__link">
				<div class="news-card__hover">
					<img src="/public/images/masks/mask-news-hover.png" alt="" />
				</div>
				<div class="news-card__content">
					<div class="news-card__preview-img">
						<div class="news-card__date">
							<span>06.10.2023</span>
						</div>
						<img :src="nextPicture" alt="news preview" />
					</div>

					<div class="news-card__info">
						<h2 class="news-card__info-title">
							{{ nextTitle }}
						</h2>
						<div
							class="news-card__info-tags news-tags"
							v-for="(tagName, index) in nextTagsNames"
							:key="tagName"
						>
							<template v-for="(color, index) in nextTagsColors" :key="color">
								<div :class="'news-tags__item--' + color[index]">
									<span>{{ tagName[index] }}</span>
								</div>
								<div :class="'news-tags__item--' + color[index + 1]">
									<!-- <img src="/public/images/icons/percent-icon.svg" alt="icon" /> -->
									<span>{{ tagName[index + 1] }}</span>
								</div>
							</template>
						</div>
					</div>
				</div>

				<button class="next-news__arrow">
					<img
						class="arrow-1056"
						src="/public/images/icons/arrow-icon.svg"
						alt="arrow button"
					/>
					<img
						class="arrow-767"
						src="/public/images/icons/arrow-icon-2.svg"
						alt="arrow button"
					/>
				</button>
				<div class="next-news__arrow-bg">
					<img src="/public/images/masks/btn-mask-767.png" />
				</div>
			</a>
		</div>
	</div>
</template>

<script setup>
const props = defineProps({
	nextTitle: { type: String },
	nextTagsNames: { type: Array },
	nextTagsColors: { type: Array },
	nextPicture: { type: String },
});
</script>

<style lang="scss" scoped></style>
