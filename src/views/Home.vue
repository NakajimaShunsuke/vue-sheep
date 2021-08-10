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
			bg-gray-200
			sm:bg-red-200
			md:bg-yellow-200
			lg:bg-green-200
			xl:bg-blue-200
		"
	>
		<!-- <img class="m-auto" alt="Vue logo" src="../assets/logo.png" />
		<HelloWorld msg="Hello Vue 3 + Vite" /> -->

		<ImageBox imgItem="/src/assets/images/main-img.jpg" />

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
			<NewsBox />
			<NewsBox />
			<NewsBox />
			<NewsBox />
		</section>
	</article>
</template>

<script setup>
import HelloWorld from "../components/HelloWorld.vue";
import ImageBox from "../components/ImageBox.vue";
import NewsBox from "../components/NewsBox.vue";
import Heading from "../components/Heading.vue";

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>
