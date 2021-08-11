<template>
	<!--
    all(mobile): bg-gray-200
    sm(min-width: 640px):red
    md(min-width: 768px):yellow
    lg(min-width: 1024px):green
    xl(min-width: 1280px):blue
  -->
	<article
		class="
			max-w-7xl
			w-full
			p-2.5
			bg-gray-200
			sm:bg-red-200
			md:bg-yellow-200
			lg:bg-green-200
			xl:bg-blue-200
		"
	>

		<!-- メインビジュアル画像 -->
		<div
			class="relative
				hidden
				sm:hidden
				md:block
				lg:block
				xl:block
			"
		>
			<ImageBox imgItem="/src/assets/images/main-img.jpg" />
			<Heading class="absolute inset-0.5"/>
		</div>

		<div
			class="
				block
				sm:block
				md:hidden
				lg:hidden
				xl:hidden
			"
		>
			<Heading class="text-gray-800" />
		</div>
		<!-- メインビジュアル画像END -->

		<section class="my-16">
			<Heading
				class="text-left"
				heading_type="h2"
				heading="Alcohol may be man’s worst enemy,but the bible says love your enemy."
			/>
			<div class="
				grid
				gap-4
				grid-cols-3
			">
				<div class="
					col-span-1
					hidden
					sm:hidden
					md:block
					lg:block
					xl:block
				"><ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" /></div>
				<div class="
					flex flex-col justify-center
					col-span-full
					sm:col-span-full
					md:col-span-2
					lg:col-span-2
					xl:col-span-2
				">
					<p v-for="text in props_text" :key="text"
						class="
							my-1.5
							text-xl
							sm:text-xl
							md:text-xl
							lg:text-2xl
							xl:text-2xl
							text-left
						"
					>
						{{ text }}
					</p>
				</div>
			</div>
		</section>


		<!--  -->
		<article>
			<Heading
				class="text-right"
				heading_type="h2"
				heading="Three elements for exploring Alcohol"
			/>
			<p v-for="text in props_text" :key="text"
				class="
					my-1.5
					text-xl
					sm:text-xl
					md:text-xl
					lg:text-2xl
					xl:text-2xl
					text-right
				"
			>
				{{ text }}
			</p>

			<TastingSection
				:props_text="props_text"
				props_heading="Color"
				props_image="/src/assets/images/3957651_s.jpg"
			/>

			<TastingSection
				:props_text="props_text"
				props_heading="Smell"
				props_image="/src/assets/images/875872_s.jpg"
			/>

			<TastingSection
				:props_text="props_text"
				props_heading="Flavor"
				props_image="/src/assets/images/4851620_s.jpg"
			/>
		</article>

		<section
		class="
			grid
			gap-4
			grid-cols-3
			w-full
			sm:w-full
			md:w-full
			lg:w-4/5
			xl:w-4/5
			m-auto
		">
			<Heading
				class="text-center col-span-full"
				heading_type="h2"
				heading="Gallery"
			/>
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
			<ImageBox imgItem="/src/assets/images/wine-6002736_640.jpg" />
		</section>

		<section
			class="
				my-4
				grid
				gap-4
				grid-cols-1
				sm:grid-cols-2
				md:grid-cols-2
				lg:grid-cols-4
				xl:grid-cols-4
			"
		>
			<div class="col-span-full"><Heading class="text-center" heading_type="h2" heading="新着情報" /></div>
			<NewsBox />
			<NewsBox />
			<NewsBox />
			<NewsBox />
		</section>

	</article>
</template>

<script setup>
import ImageBox from "../components/ImageBox.vue";
import NewsBox from "../components/NewsBox.vue";
import Heading from "../components/Heading.vue";
import TastingSection from "../components/TastingSection.vue";

const props_text = [
	'酒は人類にとって最悪の敵だが、聖書曰く、汝の敵を愛せよ、とのことだ',
	'限られた一生の中でお酒と過ごす時間を私は後悔していません',
	'色・香り・味をその一滴に感じましょう',
	'私の味わったお酒を皆様にお届けいたします'
]

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>
