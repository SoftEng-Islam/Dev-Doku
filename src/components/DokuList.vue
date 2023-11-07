<script setup lang="ts">
</script>
<template lang="pug">
//- All Docs List
div(class="absolute w-52 h-full z-10 p-4 left-0 bg-[var(--cD3)]")
	div(class="mx-auto")
		input(type="text", placeholder="Search..." value="" , class="w-full h-8 px-2 rounded-md bg-[var(--cD1)] text-white" )
	div(class="")
		ul(class="w-full flex  p-5 flex-col justify-center gap-y-4")
			li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
			li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
	button(type="button" id="closeOrResize" class="w-4 h-11 rounded-tr-lg rounded-br-lg bg-[var(--cD3)] absolute top-1/2 right-[-1rem] translate-y-[-50%]")
</template>