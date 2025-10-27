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

<div id="bigDisclaimer">
	<p>[temporary design - <b>NOT SUITABLE FOR MOBILE DEVICES</b>]</p>
</div>

<div id="header">
	<img id="pfp" alt="GitHub profile picture - my pet dog, Gina" src="https://avatars.githubusercontent.com/u/104278083">
	<div id="headerText">
		<h1>kresimirko</h1>
		<h2>Luka Krešimir Mihovilović</h2>
	</div>
	<div id="headerBg"></div>
</div>

<div id="main">
	<h1>Works</h1>

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
	#bigDisclaimer {
		padding: 0 1rem 0 1rem;
		display: flex;
		justify-content: center;
		background-color: var(--error);
		color: var(--base);
	}

	#header {
		background-color: var(--base-tp);
		padding: 6rem 10rem 2rem 10rem;
		display: flex;
		flex-direction: row;
		gap: 3rem;
		position: relative;
	}

	#headerBg {
		background-image: url("https://images.unsplash.com/photo-1506905925346-21bda4d32df4?ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&q=80&w=2070"); /* scaled-down version */
		background-repeat: no-repeat;
		background-size: cover;
		background-position: 0 30%;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: -1;
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
		padding: 3rem 10rem 3rem 10rem;
	}
</style>
