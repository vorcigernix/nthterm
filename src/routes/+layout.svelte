<script>
	import "../app.css";
	import Navbar from "../lib/navbar.svelte";
</script>

<Navbar open={false} />
<div class="space-y-8 md:space-y-16 dark:dark:bg-gray-800 dark:dark:text-gray-100">
	<slot />
</div>
