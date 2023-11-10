<script setup lang="ts">
import { appWindow } from '@tauri-apps/api/window'
import { ref } from 'vue';

function minimize(): void {
	appWindow.minimize();
}

async function maximize()  {
	await appWindow.toggleMaximize();
}
function close(): void {
	appWindow.close();
}


let darkModeChecked =  ref<boolean>(true);

function MT_toggleMode() {
	if(darkModeChecked.value === true) {
		// dark
		document.documentElement.classList.add('dark');
		console.log("dark");
	} else {
		// light
		document.documentElement.classList.remove('dark');
		console.log("light");
	}
};

let LiColorActive = ref<number>(1);

let rootElement = document.querySelector(":root") as HTMLElement;
function setColorTheme(color: number): void {
	LiColorActive.value = color;
	switch(color) {
	case 1:
		rootElement.style.setProperty("--favColor", '--gra');
		// Dark
		rootElement.style.setProperty("--borderFavColor", 'var(--bor_gra)');
		rootElement.style.setProperty("--Theme1", 'var(--th_gra1)');
		rootElement.style.setProperty("--Theme2", 'var(--th_gra2)');
		rootElement.style.setProperty("--Theme3", 'var(--th_gra3)');
		rootElement.style.setProperty("--Theme4", 'var(--th_gra4)');
		// Light
		rootElement.style.setProperty("--LborderFavColor", 'var(--gra)');
		rootElement.style.setProperty("--LTheme1", 'var(--Lth_gra1)');
		rootElement.style.setProperty("--LTheme2", 'var(--Lth_gra2)');
		rootElement.style.setProperty("--LTheme3", 'var(--Lth_gra3)');
		rootElement.style.setProperty("--LTheme4", 'var(--Lth_gra4)');
		break;
	case 2:
		rootElement.style.setProperty("--favColor", '--pur');
		// Dark
		rootElement.style.setProperty("--borderFavColor", 'var(--bor_pur)');
		rootElement.style.setProperty("--Theme1", 'var(--th_pur1)');
		rootElement.style.setProperty("--Theme2", 'var(--th_pur2)');
		rootElement.style.setProperty("--Theme3", 'var(--th_pur3)');
		rootElement.style.setProperty("--Theme4", 'var(--th_pur4)');
		// Light
		rootElement.style.setProperty("--LborderFavColor", 'var(--pur)');
		rootElement.style.setProperty("--LTheme1", 'var(--Lth_pur1)');
		rootElement.style.setProperty("--LTheme2", 'var(--Lth_pur2)');
		rootElement.style.setProperty("--LTheme3", 'var(--Lth_pur3)');
		rootElement.style.setProperty("--LTheme4", 'var(--Lth_pur4)');
		break;
	case 3:
		rootElement.style.setProperty("--favColor", '--pin');
		// Dark
		rootElement.style.setProperty("--borderFavColor", 'var(--bor_pin)');
		rootElement.style.setProperty("--Theme1", 'var(--th_pin1)');
		rootElement.style.setProperty("--Theme2", 'var(--th_pin2)');
		rootElement.style.setProperty("--Theme3", 'var(--th_pin3)');
		rootElement.style.setProperty("--Theme4", 'var(--th_pin4)');
		// Light
		rootElement.style.setProperty("--LborderFavColor", 'var(--pin)');
		rootElement.style.setProperty("--LTheme1", 'var(--Lth_pin1)');
		rootElement.style.setProperty("--LTheme2", 'var(--Lth_pin2)');
		rootElement.style.setProperty("--LTheme3", 'var(--Lth_pin3)');
		rootElement.style.setProperty("--LTheme4", 'var(--Lth_pin4)');
		break;
	case 4:
		rootElement.style.setProperty("--favColor", '--blu');
		// Dark
		rootElement.style.setProperty("--borderFavColor", 'var(--bor_blu)');
		rootElement.style.setProperty("--Theme1", 'var(--th_blu1)');
		rootElement.style.setProperty("--Theme2", 'var(--th_blu2)');
		rootElement.style.setProperty("--Theme3", 'var(--th_blu3)');
		rootElement.style.setProperty("--Theme4", 'var(--th_blu4)');
		// Light
		rootElement.style.setProperty("--LborderFavColor", 'var(--blu)');
		rootElement.style.setProperty("--LTheme1", 'var(--Lth_blu1)');
		rootElement.style.setProperty("--LTheme2", 'var(--Lth_blu2)');
		rootElement.style.setProperty("--LTheme3", 'var(--Lth_blu3)');
		rootElement.style.setProperty("--LTheme4", 'var(--Lth_blu4)');

		break;
	case 5:
		rootElement.style.setProperty("--favColor", '--gre');
		// Dark
		rootElement.style.setProperty("--borderFavColor", 'var(--bor_gre)');
		rootElement.style.setProperty("--Theme1", 'var(--th_gre1)');
		rootElement.style.setProperty("--Theme2", 'var(--th_gre2)');
		rootElement.style.setProperty("--Theme3", 'var(--th_gre3)');
		rootElement.style.setProperty("--Theme4", 'var(--th_gre4)');
		// Light
		rootElement.style.setProperty("--LborderFavColor", 'var(--gre)');
		rootElement.style.setProperty("--LTheme1", 'var(--Lth_gre1)');
		rootElement.style.setProperty("--LTheme2", 'var(--Lth_gre2)');
		rootElement.style.setProperty("--LTheme3", 'var(--Lth_gre3)');
		rootElement.style.setProperty("--LTheme4", 'var(--Lth_gre4)');
		break;
	case 6:
		rootElement.style.setProperty("--favColor", '--yel');
		// Dark
		rootElement.style.setProperty("--borderFavColor", 'var(--bor_yel)');
		rootElement.style.setProperty("--Theme1", 'var(--th_yel1)');
		rootElement.style.setProperty("--Theme2", 'var(--th_yel2)');
		rootElement.style.setProperty("--Theme3", 'var(--th_yel3)');
		rootElement.style.setProperty("--Theme4", 'var(--th_yel4)');
		// Light
		rootElement.style.setProperty("--LborderFavColor", 'var(--yel)');
		rootElement.style.setProperty("--LTheme1", 'var(--Lth_yel1)');
		rootElement.style.setProperty("--LTheme2", 'var(--Lth_yel2)');
		rootElement.style.setProperty("--LTheme3", 'var(--Lth_yel3)');
		rootElement.style.setProperty("--LTheme4", 'var(--Lth_yel4)');
	}
}
</script>
<template lang="pug">
//- Our Header
header(class="overflow-hidden w-full top-0 left-0 h-[var(--HeaderHeight)] flex items-center px-4 bg-[var(--LTheme1)] dark:bg-[var(--Theme1)]" data-tauri-drag-region style="user-select: none;")
	//- App Name or The Logo
	h1(class="text-black dark:text-white font-bold mr-auto") Dev-Doku


	//- Settings
	button(type="button", class="w-7 h-7 mx-2 rounded-full flex items-center justify-center bg-[var(--LTheme4)] dark:bg-[var(--Theme4)]")
		<i class="ri-settings-2-line ri-lg text-black dark:text-white animate__animated animate__heartBeat animate__infinite"></i>
	//- Change App Colors and Theme
	div(class="px-2 h-8 overflow-hidden rounded-full flex items-center justify-center gap-2 bg-[var(--Theme3)]")
		button(type="button", @click="setColorTheme(1)" :class="LiColorActive === 1 ? 'scale-125 mx-2': ''" class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 	bg-[var(--gra)]")
		button(type="button", @click="setColorTheme(2)" :class="LiColorActive === 2 ? 'scale-125 mx-2': ''" class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150 	bg-[var(--pur)]")
		button(type="button", @click="setColorTheme(3)" :class="LiColorActive === 3 ? 'scale-125 mx-2': ''" class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150	bg-[var(--pin)]")
		button(type="button", @click="setColorTheme(4)" :class="LiColorActive === 4 ? 'scale-125 mx-2': ''" class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150	bg-[var(--blu)]")
		button(type="button", @click="setColorTheme(5)" :class="LiColorActive === 5 ? 'scale-125 mx-2': ''" class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150	bg-[var(--gre)]")
		button(type="button", @click="setColorTheme(6)" :class="LiColorActive === 6 ? 'scale-125 mx-2': ''" class="w-5 h-5 rounded-full cursor-pointer hover:scale-90 duration-150	bg-[var(--yel)]")

	//- Dark / Light Button
	div(class="toggleMode h-7 w-16 mx-3 flex flex-row items-center justify-center rounded-full bg-[var(--Theme4)] scale-95" @click="darkModeChecked = !darkModeChecked; MT_toggleMode();")
		input(type="checkbox" :checked="darkModeChecked")
		label(for="darkmode-toggle")
			<svg viewBox="0 0 24 24" class="sun pl-[3px]" xmlns="http://www.w3.org/2000/svg"><path d="M12 18C8.68629 18 6 15.3137 6 12C6 8.68629 8.68629 6 12 6C15.3137 6 18 8.68629 18 12C18 15.3137 15.3137 18 12 18ZM12 16C14.2091 16 16 14.2091 16 12C16 9.79086 14.2091 8 12 8C9.79086 8 8 9.79086 8 12C8 14.2091 9.79086 16 12 16ZM11 1H13V4H11V1ZM11 20H13V23H11V20ZM3.51472 4.92893L4.92893 3.51472L7.05025 5.63604L5.63604 7.05025L3.51472 4.92893ZM16.9497 18.364L18.364 16.9497L20.4853 19.0711L19.0711 20.4853L16.9497 18.364ZM19.0711 3.51472L20.4853 4.92893L18.364 7.05025L16.9497 5.63604L19.0711 3.51472ZM5.63604 16.9497L7.05025 18.364L4.92893 20.4853L3.51472 19.0711L5.63604 16.9497ZM23 11V13H20V11H23ZM4 11V13H1V11H4Z"/></svg>
			<svg viewBox="0 0 24 24" class="moon pb-[2px]" xmlns="http://www.w3.org/2000/svg"><path d="M10 7C10 10.866 13.134 14 17 14C18.9584 14 20.729 13.1957 21.9995 11.8995C22 11.933 22 11.9665 22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C12.0335 2 12.067 2 12.1005 2.00049C10.8043 3.27098 10 5.04157 10 7ZM4 12C4 16.4183 7.58172 20 12 20C15.0583 20 17.7158 18.2839 19.062 15.7621C18.3945 15.9187 17.7035 16 17 16C12.0294 16 8 11.9706 8 7C8 6.29648 8.08133 5.60547 8.2379 4.938C5.71611 6.28423 4 8.9417 4 12Z"/></svg>


	//- titlebar buttons
	div(class="flex items-center justify-center gap-2 ml-4")
		button(type="button" @click="minimize" class="w-6 h-6 rounded-md cursor-pointer hover:opacity-50 bg-yellow-500")
			<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="white"><path d="M12 16L6 10H18L12 16Z"/></svg>
		button(type="button" @click="maximize" class="w-6 h-6 rounded-md cursor-pointer hover:opacity-50 bg-green-500")
			<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" fill="white"><path d="M12 8L18 14H6L12 8Z"/></svg>
		button(type="button" @click="close" class="w-6 h-6 rounded-md cursor-pointer hover:opacity-50 bg-red-500")
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 200" fill="white" stroke="white" stroke-width="2"><path d="M114,100l49-49a9.9,9.9,0,0,0-14-14L100,86,51,37A9.9,9.9,0,0,0,37,51l49,49L37,149a9.9,9.9,0,0,0,14,14l49-49,49,49a9.9,9.9,0,0,0,14-14Z"/></svg>

</template>
<style scoped lang="scss">
.toggleMode {
	input {
		@apply w-0 h-0;
		visibility: hidden;
		&:checked + label {
			@apply bg-[var(--Theme4)];
		}
		&:checked + label:after {
			@apply left-full;
			transform: translateX(-100%);
			background: linear-gradient(180deg,#868686,#8D5EB9);
		}
		&:checked + label svg.sun {
			@apply fill-gray-400
		}
		&:checked + label svg.moon {
			@apply fill-white;
		}
	}

	label {
		@apply w-full h-full relative flex flex-row items-center justify-center rounded-full cursor-pointer duration-300;
		&:after {
			content: "";
			@apply w-8 h-8 absolute left-0 rounded-full duration-300;
			background: linear-gradient(180deg,#ffcc89,#c3790c);
			box-shadow: 0px 5px 10px rgba(0,0,0,0.2);
		}
		& svg {
			@apply absolute w-7 z-10;
		}
		& svg.sun {
			@apply left-0 fill-white duration-300;
		}
		& svg.moon {
			@apply  right-0 fill-gray-400 duration-300;
		}
		&:active:after{
			@apply w-10;
		}
	}
}
</style>
