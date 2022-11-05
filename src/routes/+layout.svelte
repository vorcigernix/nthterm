<script>
	import "../app.css";
	import Navbar from "../lib/navbar.svelte";
</script>

<Navbar open={false} />
<div class="space-y-8 md:space-y-16">
	<slot />
</div>
