<template>
<h1 ><span>{{heading_span}}</span>{{heading}}</h1>
</template>
<script setup="props">
import { defineProps } from "vue";
defineProps({
	heading: { type: String, default: "これは見出しです" },
  heading_span: { type: String, default: "これはサブ見出しです" },
})
</script>
<style scoped>
h1 {
  text-align: left;
	font-size: 24px;
}

h1 span {
	display: flex;
	align-items: center;
	color: #2c3e50;
	font-size: 16px;
	text-transform: uppercase;
}

h1 span::before {
	content: '';
	display: inline-block;
	margin-right: 10px;
	width: 25px;
	height: 1px;
	background-color: #2c3e50;
}
</style>