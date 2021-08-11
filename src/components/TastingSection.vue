<template>
		<section class="my-16">
			<Heading
				class="text-right"
				heading_type="h2"
				:heading="props_heading"
			/>
			<div class="
				grid
				gap-4
				grid-cols-3
			">
				<div class="
					flex flex-col
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
				<div class="
					col-span-1
					hidden
					sm:hidden
					md:block
					lg:block
					xl:block
				"><ImageBox :imgItem="props_image" /></div>
			</div>
		</section>
</template>
<script setup="props">
import Heading from "./Heading.vue";
import ImageBox from "./ImageBox.vue";

import { defineProps } from "vue";
defineProps({
  props_text: {
    type: Array,
    default: () => []
  },
  props_heading: { type: String, default: "Alcohol may be man’s worst enemy,but the bible says love your enemy." },
  props_image: { type: String, default:"" }
})
</script>