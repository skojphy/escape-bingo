<script>
	export let isChecked = false;
	export let themeName = '테마가 없습니다';
	const n = 1;
	const onClick = () => {
		isChecked = !isChecked;
	};
</script>

<li>
	<button
		class={isChecked ? 'checked' : 'notChecked'}
		on:click={onClick}
		aria-pressed={isChecked}
	>
		<span>{themeName}</span>
	</button>
</li>

<style>
	li {
		width: 100%;
		/* height: 100%; */
		position: relative;
		box-sizing: border-box;
		border: 1px solid #000;
		font-size: 14px;
		font-weight: bold;
		line-height: 17px;
		padding: 0;
		color: rgb(119, 119, 119);
		background: rgb(228, 228, 228);
		padding: 2px;
		display: block;
		padding: 0;
		min-width: 60px;
		min-height: 60px;
		border: 1px solid black;
	}
	li::after {
		display: block;
		content: '';
		padding-bottom: 100%;
	}
	button {
		position: absolute;
		width: 100%;
		height: 100%;
		border: none;
	}
	.checked {
		background: #234baf;
		color: #fff;
		font-weight: 700;
	}
	span {
		@media only screen and (max-width: 400px) {
			font-size: 10px;
			line-height: 12px;
		}
		@media only screen and (min-width: 401px) and (max-width: 600px) {
			font-size: 12px;
			line-height: 15px;
		}
		@media only screen and (min-width: 601px) {
			font-size: 15px;
			line-height: 20px;
		}
		word-break: keep-all;
	}
</style>
