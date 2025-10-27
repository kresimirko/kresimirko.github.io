<script lang="ts">
	function setTheme(themeName: string) {
		localStorage.setItem('theme', themeName);
		document.documentElement.className = themeName;
	}
	function toggleTheme() {
		setTheme(localStorage.getItem('theme') === 'theme-dark' ? 'theme-light' : 'theme-dark');
	}
</script>

<h1>kresimirko.github.io</h1>

<p>[temporary website]</p>

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
