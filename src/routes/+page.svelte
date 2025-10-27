<script lang="ts">
	function setTheme(themeName: string) {
		localStorage.setItem('theme', themeName);
		document.documentElement.className = themeName;
	}
	function toggleTheme() {
		setTheme(localStorage.getItem('theme') === 'theme-dark' ? 'theme-light' : 'theme-dark');
	}
</script>

<svelte:head>
	<title>kresimirko's site</title>
</svelte:head>

<div id="header">
	<img id="pfp" alt="GitHub profile picture - my pet dog, Gina" src="https://avatars.githubusercontent.com/u/104278083">
	<div id="headerText">
		<h1>kresimirko</h1>
		<h2>Luka Krešimir Mihovilović</h2>
	</div>
</div>

<div id="main">
	<p>[temporary website - <b>NOT SUITABLE FOR MOBILE DEVICES</b>]</p>

	<h2>Works</h2>

	<p><a href="./kikipnt/">kikipnt</a></p>
	<p><a href="./digitalizacija-tv/">Digitalizacija televizije</a></p>
	<p><a href="./karta-trogira/">Karta gradske jezgre Trogira</a></p>

	<hr />

	<div style="font-size: small;">
		<p>
			this site uses the <a href="https://catppuccin.com/palette/">catppuccin</a> color palette
			&bullet; <a href="#" onclick={toggleTheme}>switch themes</a>
			&bullet; <a href="https://github.com/kresimirko/kresimirko.github.io">view this site's source</a>
		</p>
		<p>&copy; kresimirko 2025</p>
	</div>
</div>

<style>
	#header {
		background-color: var(--mantle);
		padding: 6rem 10rem 2rem 10rem;
		display: flex;
		flex-direction: row;
		gap: 3rem;
	}

	#headerText {
		display: flex;
		flex-direction: column;
		min-height: 0;
		justify-content: end;
	}

	#headerText h1 {
		font-weight: 100;
		font-size: 5rem;
		margin: 0;
		padding: 0;
	}

	#headerText h2 {
		font-weight: 300;
		font-size: 2rem;
		margin: 0;
		padding: 0 0 0 5px; /* optical stabilization...? */
	}

	#pfp {
		border-radius: 100% 100% 25% 100%;
		max-width: 16rem;
	}

	#main {
		padding: 1rem 10rem 3rem 10rem;
	}
</style>
