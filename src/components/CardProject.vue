<template>
	<RouterLink :to="to" class="card w-60 rounded-sm image-full shadow-xl h-44">
		<figure v-if="imagen">
			<img :src="imagen" alt="title" />
		</figure>
		<div class="card-body">
			<h2 class="card-title">{{ title }}</h2>
			<p>{{ desc }}</p>
		</div>
	</RouterLink>
</template>

<script setup>
import { ref } from "vue";

const props = defineProps({
	title: String,
	desc: String,
	imagen: String,
	to: {
		type: String,
		required: true,
	},
});
</script>
