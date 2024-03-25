<script>
	import '../app.css';
	import {
		Navbar,
		NavBrand,
		NavLi,
		NavUl,
		NavHamburger,
		ImagePlaceholder,
		Skeleton,
		TextPlaceholder
	} from 'flowbite-svelte';

	import { DarkMode } from 'flowbite-svelte';
	import { Button } from 'flowbite-svelte';
	let btnClass =
		'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2';
    let navBtnClass = 'hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg';
</script>

<div class="relative px-8">
	<Navbar class="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 start-0 border-b">
		<NavBrand href="/">
			<img src="../../img/navicon_w.png" class="me-3 h-6 sm:h-9" alt="Logo BMKG" />
			<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
				>Lightning Detector</span
			>
		</NavBrand>

		<NavHamburger />
		<NavUl class="flex flex-wrap gap-2">
			<div class="flex flex-wrap gap-2">
				<Button color="none" class={navBtnClass} href="/" active={true}>Home</Button>
				<Button color="none" class={navBtnClass} href="/about">About</Button>
				<Button color="none" class={navBtnClass} href="/docs/components/navbar">Navbar</Button>
				<Button color="none" class={navBtnClass} href="/pricing">Pricing</Button>
				<Button color="none" class={navBtnClass} href="/contact">Contact</Button>
				<DarkMode {btnClass} />
			</div>
		</NavUl>
	</Navbar>
	<div>
		<!-- <Skeleton class="mt-16 mb-8" />
		<ImagePlaceholder class="my-8" />
		<TextPlaceholder class="my-8" /> -->
	</div>
</div>
<div class="mt-20"></div>
<slot />
