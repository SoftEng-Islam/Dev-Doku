<script setup lang="ts">
import { appWindow } from '@tauri-apps/api/window'
function minimize(): void {
	appWindow.minimize();
}

async function maximize()  {
	await appWindow.toggleMaximize();
}
function close(): void {
	appWindow.close();
}
</script>
<template lang="pug">
//- Our Header
header(class="overflow-hidden w-full top-0 left-0 h-[var(--HeaderHeight)] flex items-center px-4 bg-[var(--cD1)]" data-tauri-drag-region style="user-select: none;")
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
	//- Settings
	//- titlebar buttons
	div(class="flex items-center justify-center gap-2 ml-4")
		button(type="button" @click="minimize" class="w-6 h-6 rounded-md cursor-pointer hover:opacity-50 bg-yellow-500")
			<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="white"><path d="M12 16L6 10H18L12 16Z"/></svg>
		button(type="button" @click="maximize" class="w-6 h-6 rounded-md cursor-pointer hover:opacity-50 bg-green-500")
			<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="white"><path d="M12 8L18 14H6L12 8Z"/></svg>
		button(type="button" @click="close" class="w-6 h-6 rounded-md cursor-pointer hover:opacity-50 bg-red-500")
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200" fill="white" stroke="white" stroke-width="2"><path d="M114,100l49-49a9.9,9.9,0,0,0-14-14L100,86,51,37A9.9,9.9,0,0,0,37,51l49,49L37,149a9.9,9.9,0,0,0,14,14l49-49,49,49a9.9,9.9,0,0,0,14-14Z"/></svg>

</template>