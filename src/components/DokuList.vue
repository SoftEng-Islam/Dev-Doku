<script setup lang="ts">
</script>
<template lang="pug">
div(class="w-52 h-full absolute bg-[var(--cD3)]")
	div(class="w-full p-5 flex items-center justify-center")
		input(type="text", placeholder="Search..." value="" , class="h-8 px-2 rounded-md bg-[var(--cD1)] text-white" )
	div(class="")
		ul(class="w-full flex  p-5 flex-col justify-center gap-y-4")
			li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")
			li(class="relative w-full h-7 rounded-md bg-[var(--cD1)] cursor-pointer ")

	div(class="w-5 h-5 bg-slate-500 absolute right-0")
</template>