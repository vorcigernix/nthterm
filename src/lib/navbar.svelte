<script>
	/**
	 * @type {boolean}
	 */
	export let open;
	import { page } from '$app/stores';
</script>

<nav class="p-4 text-gray-100 sticky top-0 z-10 md:bg-black/50 bg-black md:backdrop-blur-md ">
	<div class="container flex justify-between h-16 mx-auto md:justify-center md:space-x-8">
		<ul class="items-stretch hidden space-x-3 md:flex">
			<li class="flex">
				<a
					href="/"
					class="flex items-center px-4 -mb-1 border-b-2 border-transparent"
					on:click={() => (open = false)}
					class:active={$page.url.pathname === '/'}>Home</a
				>
			</li>
			<li class="flex">
				<a
					href="/mentors"
					on:click={() => (open = false)}
					class:active={$page.url.pathname === '/mentors'}
					class="flex items-center px-4 -mb-1 border-b-2 border-transparent">Mentors</a
				>
			</li>
			<li class="flex">
				<a
					href="/sessions"
					on:click={() => (open = false)}
					class:active={$page.url.pathname === '/sessions'}
					class="flex items-center px-4 -mb-1 border-b-2 border-transparent">My Sessions</a
				>
			</li>
		</ul>
		<a href="/" aria-label="Back to homepage" class="flex items-center p-2">
			<svg
				fill="currentColor"
				viewBox="0 0 32 32"
				class="w-8 h-8 text-lime-500"
				xmlns="http://www.w3.org/2000/svg"
			>
				<path
					d="M27.912 7.289l-10.324-5.961c-0.455-0.268-1.002-0.425-1.588-0.425s-1.133 0.158-1.604 0.433l0.015-0.008-10.324 5.961c-0.955 0.561-1.586 1.582-1.588 2.75v11.922c0.002 1.168 0.635 2.189 1.574 2.742l0.016 0.008 10.322 5.961c0.455 0.267 1.004 0.425 1.59 0.425 0.584 0 1.131-0.158 1.602-0.433l-0.014 0.008 10.322-5.961c0.955-0.561 1.586-1.582 1.588-2.75v-11.922c-0.002-1.168-0.633-2.189-1.573-2.742zM27.383 21.961c0 0.389-0.211 0.73-0.526 0.914l-0.004 0.002-10.324 5.961c-0.152 0.088-0.334 0.142-0.53 0.142s-0.377-0.053-0.535-0.145l0.005 0.002-10.324-5.961c-0.319-0.186-0.529-0.527-0.529-0.916v-11.922c0-0.389 0.211-0.73 0.526-0.914l0.004-0.002 10.324-5.961c0.152-0.090 0.334-0.143 0.53-0.143s0.377 0.053 0.535 0.144l-0.006-0.002 10.324 5.961c0.319 0.185 0.529 0.527 0.529 0.916z"
					style="fill: rgb(186, 218, 85);"
				/>
				<polygon
					points="20.406 11.295 18.286 17.655 11.926 19.775 14.046 13.415 20.406 11.295"
					style="fill: none; stroke: rgb(186, 218, 85); stroke-width: 2px;"
				/>
			</svg>
		</a>
		<ul class="items-stretch hidden space-x-3 md:flex">
			<li class="flex">
				<a
					href="/topics"
					on:click={() => (open = false)}
					class:active={$page.url.pathname === '/topics'}
					class="flex items-center px-4 -mb-1 border-b-2 border-transparent">Topics</a
				>
			</li>
			<li class="flex">
				<a
					href="/about"
					on:click={() => (open = false)}
					class:active={$page.url.pathname === '/about'}
					class="flex items-center px-4 -mb-1 border-b-2 border-transparent">About</a
				>
			</li>
			<li class="flex">
				<button class="flex items-center px-4 -mb-1 border-b-2 border-transparent">Connect</button>
			</li>
		</ul>
		<button class="p-4 md:hidden" on:click={() => (open = !open)}>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
				class="w-6 h-6 text-gray-100"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M4 6h16M4 12h16M4 18h16"
				/>
			</svg>
		</button>
	</div>
	<ul class={open ? `flex flex-col pt-20 space-y-8 min-h-screen md:hidden text-xl font-bold items-center` : `hidden`}>
		<li class="flex">
			<a
				href="/"
				class="flex items-center px-4 -mb-1 border-b-2 border-transparent"
				on:click={() => (open = false)}
				class:active={$page.url.pathname === '/'}>Home</a
			>
		</li>
		<li class="flex">
			<a
				href="/mentors"
				on:click={() => (open = false)}
				class:active={$page.url.pathname === '/mentors'}
				class="flex items-center px-4 -mb-1 border-b-2 border-transparent">Mentors</a
			>
		</li>
		<li class="flex">
			<a
				href="/sessions"
				on:click={() => (open = false)}
				class:active={$page.url.pathname === '/sessions'}
				class="flex items-center px-4 -mb-1 border-b-2 border-transparent">My Sessions</a
			>
		</li>
		<li class="flex">
			<a
				href="/topics"
				on:click={() => (open = false)}
				class:active={$page.url.pathname === '/topics'}
				class="flex items-center px-4 -mb-1 border-b-2 border-transparent">Topics</a
			>
		</li>
		<li class="flex">
			<a
				href="/about"
				on:click={() => (open = false)}
				class:active={$page.url.pathname === '/about'}
				class="flex items-center px-4 -mb-1 border-b-2 border-transparent">About</a
			>
		</li>
		<li class="flex">
			<button class="flex items-center px-4 -mb-1 border-b-2 border-transparent">Connect</button>
		</li>
	</ul>
</nav>

<style>
	.active {
		@apply text-lime-400 border-lime-400;
	}
</style>
