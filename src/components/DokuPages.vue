<script setup lang="ts">
</script>
<template lang="pug">
div(class="w-52 h-full absolute left-52 bg-[var(--cD2)]")
	div(class="w-full flex items-center justify-center")
		input(type="text", placeholder="Search..." value="" , class="h-8 px-2 rounded-md bg-[var(--cD1)] text-white" )
	div(class="")
		ul(class="w-full flex  p-5 flex-col justify-center gap-y-4")
			li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
			li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
	button(type="button" id="closeOrResize" class="w-4 h-11 rounded-tr-lg rounded-br-lg bg-[var(--cD2)] absolute top-1/2 right-[-1rem] translate-y-[-50%]")
</template>