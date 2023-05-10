<script>
	import '../app.scss';
</script>

<div id="wrapper">
	<header><h1>헤딩</h1></header>
	<main><slot /></main>
	<footer>
		<nav>
			<a href="https://seohey.tistory.com/" target="_blank">Blog</a> |
			<a href="https://github.com/skojphy" target="_blank">Github</a> |
			<a href="https://www.instagram.com/seo__hey/" target="_blank">Instagram</a
			>
		</nav>
		<p>
			<span>seohey@kakao.com</span>
			<br />
			<span>© 2023. seohey. All Rights Reserved.</span>
		</p>
	</footer>
</div>

<style>
	@font-face {
		font-family: 'TAEBAEKmilkyway';
		src: url('https://cdn.jsdelivr.net/gh/projectnoonnu/noonfonts_2302@1.0/TAEBAEKmilkyway.woff2')
			format('woff2');
		font-weight: normal;
		font-style: normal;
	}

	:global(*) {
		font-family: 'TAEBAEKmilkyway', sans-serif;
	}

	:global(ol, ul) {
		list-style: none;
	}

	#wrapper {
		min-height: 100vh;
		position: relative;
		width: 100%;
	}

	h1 {
		font-size: 20px;
	}

	main {
		display: flex;
		justify-content: center;
		box-sizing: border-box;
		padding: 90px 0 90px 0;
	}
	header,
	footer {
		background-color: #333;
		color: white;
		text-align: center;
		width: 100%;
		position: absolute;
		box-sizing: border-box;
	}
	header {
		top: 0px;
		height: 50px;
		line-height: 50px;
	}
	footer {
		height: 90px;
		bottom: 0px;
		padding: 15px;
		line-height: 20px;
	}
	footer a {
		color: #fff;
	}
</style>
