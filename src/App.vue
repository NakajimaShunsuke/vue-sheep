<template>
  <router-view class="base-layout responsive-tools" />
</template>

<script setup>

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Shippori+Mincho&display=swap');

/**
 * This injects Tailwind's base styles and any base styles registered by
 * plugins.
 */
@tailwind base;

/**
 * This injects Tailwind's component classes and any component classes
 * registered by plugins.
 */
@tailwind components;

/**
 * This injects Tailwind's utility classes and any utility classes registered
 * by plugins.
 */
@tailwind utilities;

/**
 * Use this directive to control where Tailwind injects the responsive
 * variations of each utility.
 *
 * If omitted, Tailwind will append these classes to the very end of
 * your stylesheet by default.
 */
 @tailwind screens;


#app {

	font-family: "Noto Serif JP","游明朝","Yu Mincho",YuMincho,"Hiragino Mincho ProN W3","ヒラギノ明朝 ProN W3","Hiragino Mincho ProN","HG明朝E","ＭＳ Ｐ明朝","ＭＳ 明朝",serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
	letter-spacing:0.1em;
	margin-top: 60px;
  display: flex;
  justify-content: center;
}

.responsive-tools {
    /**
			all(mobile): bg-gray-200
			sm(min-width: 640px):red
			md(min-width: 768px):yellow
			lg(min-width: 1024px):green
			xl(min-width: 1280px):blue
		*/
	@apply bg-gray-200 sm:bg-red-200 md:bg-yellow-200 lg:bg-green-200 xl:bg-blue-200;
}
.base-layout {
	@apply max-w-7xl w-full p-2.5;
}
</style>
