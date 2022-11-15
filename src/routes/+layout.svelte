<script>
	import '../app.css';
	const inactiveLinkClass =
		'text-left text-limed-spruce-500 hover:text-regent-st-blue-500 text-xl col-span-1 md:col-span-6 justify-start';
	const activeLinkClass =
		'text-left text-regent-st-blue-500 text-xl col-span-1 md:col-span-6 justify-start';

	let current = 'index';
</script>

<nav class="not-prose md:grid md:grid-cols-6">
	<a
		href="/"
		class={current === 'index' ? activeLinkClass : inactiveLinkClass}
		on:click={() => (current = 'index')}>Home</a
	>
	<a
		href="/about"
		class={current === 'about' ? activeLinkClass : inactiveLinkClass}
		on:click={() => (current = 'about')}>About</a
	>
	<a
		href="/settings"
		class={current === 'settings' ? activeLinkClass : inactiveLinkClass}
		on:click={() => (current = 'settings')}>Settings</a
	>
</nav>

<slot />
