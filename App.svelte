<script>
	
	import {page_shown} from "./data"
	
	import Nav from "./Nav.svelte"
	import Index from "./Index.svelte"
	import ContactUs from "./Contact-us.svelte"
	import AboutUs from "./About-us.svelte"

	history.replaceState({"href_to_show":"/"}, "", "/")

	window.addEventListener("popstate", e => {
		console.log(e.state.href_to_show)
		$page_shown = e.state.href_to_show
	})


</script>

<Nav />

{#if $page_shown == "/"}
	<Index />
{/if}

{#if $page_shown == "about-us"}
	<AboutUs />
{/if}

{#if $page_shown == "contact-us"}
	<ContactUs />
{/if}



<style>

</style>