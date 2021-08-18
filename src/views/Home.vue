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
		<!-- Maineセクション -->
		<section>
			<h1 class="text-2xl lg:text-4xl mb-2">Civilization begins with distillation.</h1>
			<p class="text-xl lg:text-2xl mb-2 font-bold">文明は蒸留から始まる</p>
			<p class="text-xl lg:text-lg">限られた人生でお酒と過ごす時間を私は後悔していません<br>
				色・香り・味をその一滴に感じましょう<br>
				私の味わったお酒を皆様にお届けいたします</p>
		</section>

	</article>
</template>

<script setup>
import ImageBox from "../components/ImageBox.vue";

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>
