<template>
	<h2 v-if="heading_type === 'h2'" class="
		m-2
		text-left
		text-2xl
		sm:text-2xl
		md:text-2xl
		lg:text-3xl
		xl:text-3xl">
	{{ heading }}
	</h2>

	<h1 v-else class="
		text-white
		text-left
		text-3xl
		sm:text-3xl
		md:text-4xl
		lg:text-5xl
		xl:text-6xl">{{ heading }}
		<span class="
		flex
		items-center
		uppercase
		text-xl
		sm:text-2xl
		md:text-2xl
		lg:text-3xl
		xl:text-3xl
	">{{ heading_span }}</span></h1>
</template>

<script setup="props">
import { defineProps } from "vue";
defineProps({
	heading: { type: String, default: "Civilization begins with distillation." },
  heading_span: { type: String, default: "文明は蒸留から始まる" },
	heading_type:{ type: String, default: "" }
})
</script>