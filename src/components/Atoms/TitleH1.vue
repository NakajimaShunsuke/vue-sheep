<template>
	<h1 class="top-title">
		{{ title }}<br />
		<span>{{ sub_title }}</span>
	</h1>
</template>

<script setup>
// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md

defineProps({
	title: { type: String, default: "" },
	sub_title: { type: String, default: "" },
});
</script>

<style scoped>
.top-title {
	@apply text-3xl md:text-5xl mb-2;
}

.top-title span {
	@apply text-2xl md:text-3xl mb-2 font-bold;
}
</style>
