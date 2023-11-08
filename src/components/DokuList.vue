<script setup lang="ts">
	import { ref } from 'vue';
	import DokuPages from "./DokuPages.vue";

	let DokuListClosed= ref<boolean>(false);
	function close(): void {
		DokuListClosed.value = !DokuListClosed.value;
	}
</script>
<template lang="pug">
//- All Docs List
div(class="absolute w-52 h-[var(--DokuListsHeight)] p-4 bg-[var(--cD3)] duration-100" :style="DokuListClosed ? 'left: -13rem' : 'left: 0'")
	div(class="z-10")
		div()
			input(type="text", placeholder="Search..." value="" , class="w-full h-8 px-2 rounded-md bg-[var(--cD1)] text-white" )
		div(class="")
			ul(class="w-full flex p-5 flex-col justify-center gap-y-4")
				li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
				li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
		button(type="button" @click="close" class="w-4 h-11 rounded-tr-lg rounded-br-lg bg-[var(--cD3)] absolute z-20 top-1/2 right-[-1rem] translate-y-[-50%]")
	<doku-pages/>
</template>