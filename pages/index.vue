<template>
	<div>
		<section class="news-popup">
			<div class="container">
				<button class="close-btn">
					<img
						class="close-btn__img"
						src="/public/images/icons/close-btn.svg"
						alt="close"
					/>
				</button>
				<div class="news-popup__header">
					<div class="news-popup__breadcrumbs">
						<div class="bred">
							<div class="bred-item">
								<span class="bred-item__text">Главная</span>
							</div>
							<div class="bred-item">
								<span class="bred-item__text">Новости</span>
							</div>
							<div class="bred-item">
								<span class="bred-item__text">
									Средняя ставка по ипотеке в России превысила 8%
								</span>
							</div>
						</div>
					</div>
				</div>

				<div class="news-popup-top">
					<div class="news-popup-top__tags news-tags">
						<div class="news-tags__item">
							<span>в СМИ</span>
						</div>
						<div class="news-tags__item">
							<img src="/public/images/icons/percent-icon.svg" alt="icon" />
							<span>акции</span>
						</div>
					</div>
					<h1 class="news-popup-top__title">
						Средняя ставка по ипотеке в России превысила 8%
					</h1>
					<div class="news-popup-top__date">06.10.2023</div>
				</div>

				<div class="news-popup-content">
					<p class="news-popup-content__text">
						Аналитики одного из ведущих игроков на российском рынке кредитования
						объясняют это завершением околонулевых программ и изменением условий по ряду
						<a
							class="news-popup-content__text-link"
							href="https://www.vtb.ru/personal/ipoteka/lgotnaya-ipoteka/"
						>
							<span>программ с господдержкой</span>
							.
						</a>
						При этом специалисты ВТБ прогнозируют в дальнейшем замедление роста средней
						ставки.
					</p>
					<img
						class="news-popup-content__img"
						src="/public/images/news-photo/playground.webp"
						alt="playground"
					/>
					<p class="news-popup-content__text">
						Если во втором полугодии прошлого года средняя ставка по ипотеке выросла до
						7,38%, к концу года упала до 6,65%, то с начала года она выросла: на 1,2
						п.п. — в январе, на 0,19 п.п. — в феврале и, по прогнозам ВТБ, на 0,26 п.п.
						— в марте.
					</p>
					<p class="news-popup-content__text">
						К концу первого квартала средняя ставка по ипотеке достигла 8,3%.
					</p>
					<p class="news-popup-content__text">
						Самая низкая ставка сейчас действует на рынке новостроек, благодаря
						программам господдержки. По оценке специалистов ВТБ, ее мартовское значение
						составило 5,5%—5,7%.
					</p>
					<p class="news-popup-content__text">
						Растущая популярность «Семейной ипотеки» в результате ее распространения на
						все семьи с двумя несовершеннолетними детьми и адаптация участников рынка к
						новым условиям «ипотеки от застройщика» помогут сбалансировать рынок
						первичной недвижимости.
					</p>
				</div>

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
								<img
									src="/public/images/news-photo/news-card-preview.webp"
									alt="news preview"
								/>
							</div>

							<div class="news-card__info">
								<h2 class="news-card__info-title">
									Правительство продлило «Льготную ипотеку» и расширило «Семейную».
								</h2>
								<div class="news-card__info-tags news-tags">
									<div class="news-tags__item">
										<span>в СМИ</span>
									</div>
									<div class="news-tags__item">
										<img src="/public/images/icons/percent-icon.svg" alt="icon" />
										<span>акции</span>
									</div>
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
		</section>
	</div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
