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
		'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2 px-3';
    let navBtnClass = 'hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg';
</script>


<!-- <div class="relative px-8"> -->
    <!-- add class fixed to make it sticky -->
	<Navbar class="px-2 sm:px-4 py-2.5 w-full z-20 top-0 start-0 border-b">
		<NavBrand href="/">
			<img src="../../img/navicon_w.png" class="me-3 h-6 sm:h-9" alt="Logo BMKG" />
			<span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
				>BMKG</span
			>
		</NavBrand>
		<NavHamburger />
		<NavUl>
			<div class="flex flex-wrap gap-2">
				<Button color="none" class={navBtnClass} href="/" active={true}>Home</Button>
				<Button color="none" class={navBtnClass} href="/test">About</Button>
				<Button color="none" class={navBtnClass} href="/dial">Navbar</Button>
				<Button color="none" class={navBtnClass} href="/sidebar">Pricing</Button>
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
    
<!-- </div> -->
<div class="my-4 mx-4">
<slot />
</div>

<!-- 
<script>
    import '../app.css';
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger, Button, Input } from 'flowbite-svelte';
  </script>
  
  <Navbar>
    <NavBrand href="/">
      <img src="/images/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Flowbite</span>
    </NavBrand>
    <div class="flex md:order-2">
      <Button size="sm">Get started</Button>
      <NavHamburger />
    </div>
    <NavUl class="order-1">
      <NavLi href="/" active={true}>Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/docs/components/navbar">Navbar</NavLi>
      <NavLi href="/pricing">Pricing</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
  </Navbar>
  test body
  <slot /> -->