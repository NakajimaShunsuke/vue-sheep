<template>
	<TitleH1 v-if="title_no === '1'" :title="title" :sub_title="sub_title" />
	<TitleH2 v-else :title="title" :sub_title="sub_title" />
</template>

<script setup>
import TitleH1 from "../Atoms/TitleH1.vue";
import TitleH2 from "../Atoms/TitleH2.vue";

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md

defineProps({
	title_no: { type: String, default: "2" },
	title: { type: String, default: "" },
	sub_title: { type: String, default: "" },
});
</script>

<style scoped></style>
