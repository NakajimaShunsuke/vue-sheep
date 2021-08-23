<template>
	<img
		class="block w-full"
		:class="{ filter: isFilter, grayscale: isGrayscale }"
		:src="imgItem"
		:alt="altText"
	/>
</template>

<script setup="props">
import { defineProps } from "vue";
defineProps({
	imgItem: { type: String, default: "" },
	altText: { type: String, default: "WEB-Image" },
	isFilter: { type: Boolean, default: true },
	isGrayscale: { type: Boolean, default: true },
});
</script>
