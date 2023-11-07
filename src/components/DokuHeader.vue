<script setup lang="ts">
</script>
<template lang="pug">
//- Our Header
header(class="h-14 flex items-center px-4 bg-[var(--cD1)]")
	//- App Name or The Logo
	h1(class="text-white") Dev-Doku
	//- Change App Colors and Theme
	ul(class="ml-auto px-2 h-8 overflow-hidden rounded-full flex items-center justify-center gap-2 bg-[var(--cD3)]")
		li(class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 bg-gray-500")
		li(class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 bg-purple-500")
		li(class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 bg-pink-500")
		li(class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 bg-blue-500")
		li(class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 bg-green-500")
		li(class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 bg-yellow-500")
</template>