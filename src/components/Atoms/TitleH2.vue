<template>
	<h2 class="top-content-title">
		<span>{{ sub_title }}</span
		>{{ title }}
	</h2>
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
.top-content-title {
	@apply text-2xl md:text-3xl font-bold;
}

.top-content-title span {
	color: #2c3e50;
	@apply flex items-center text-xl md:text-2xl uppercase;
}

.top-content-title span::before {
	content: "";
	background-color: #2c3e50;
	@apply inline-block m-1 w-10 h-px;
}
</style>
