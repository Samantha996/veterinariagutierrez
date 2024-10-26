<script>
	// for more grass
	(function () {
		function getRndNum(min, max) {
			return Math.round(Math.random() * (max - min)) + min;
		}
		for (let x = 0; x < 120; x += getRndNum(2, 6)) {
			let rndNum = getRndNum(70, 100);
			let el = document.createElement('div');
			el.classList.add('grass');
			el.style.width = rndNum + 'vmin';
			el.style.height = rndNum + 'vmin';
			for (let y = 0; y < 3; y++) {
				let blade = document.createElement('div');
				blade.classList.add('grass__blade--' + (y + 1));
				blade.classList.add('grass__blade');
				blade.style.setProperty('animation-delay', x + '0ms');
				el.appendChild(blade);
			}
			el.style.left = x + 'vw';
			document.querySelector('body').appendChild(el);
		}
	})();
</script>

<div class="grass h-5 w-full">
	<div class="grass__blade grass__blade--3"></div>
</div>

<style lang="scss">
	$clr: darken(#339545, 10%);

	body {
		background: #688acc;
	}

	body {
		height: 100vh;
		overflow: hidden;
	}

	.grass {
		width: 100vmin;
		height: 100vmin;
		position: absolute;
		overflow: hidden;
		transform: translate(-50%, 0%) translate3d(0, 0, 0);
		bottom: 0;
	}

	.grass__blade {
		position: absolute;

		&--1 {
			border-right: 3vmin solid $clr;
			border-top-right-radius: 50%;
			height: 160%;
			width: 100%;
			bottom: -100%;
			left: -50%;
			animation: move-blade-1 60s infinite;
		}

		@keyframes move-blade-1 {
			0%,
			30%,
			50%,
			55%,
			82%,
			97%,
			100% {
				border-top-right-radius: 50%;
			}
			20% {
				border-top-right-radius: 30%;
			}
			40% {
				border-top-right-radius: 20%;
			}
			70% {
				border-top-right-radius: 25%;
			}
			90% {
				border-top-right-radius: 35%;
			}
		}

		&--2 {
			border-right: 3vmin solid $clr;
			border-top-right-radius: 20%;
			height: 300%;
			width: 200%;
			bottom: -230%;
			left: -150%;
			animation: move-blade-2 60s infinite;
		}

		@keyframes move-blade-2 {
			0%,
			30%,
			50%,
			55%,
			82%,
			97%,
			100% {
				border-top-right-radius: 20%;
			}
			20% {
				border-top-right-radius: 15%;
			}
			40% {
				border-top-right-radius: 10%;
			}
			70% {
				border-top-right-radius: 10.5%;
			}
			90% {
				border-top-right-radius: 12.5%;
			}
		}

		&--3 {
			border-top-left-radius: 15%;
			border-left: 3vmin solid $clr;
			height: 360%;
			width: 200%;
			bottom: -300%;
			left: 50%;
			animation: move-blade-3 60s infinite;
		}
		@keyframes move-blade-3 {
			0%,
			30%,
			50%,
			55%,
			82%,
			97%,
			100% {
				border-top-left-radius: 15%;
			}
			20% {
				border-top-left-radius: 22%;
			}
			40% {
				border-top-left-radius: 17.5%;
			}
			70% {
				border-top-left-radius: 18.5%;
			}
			90% {
				border-top-left-radius: 21%;
			}
		}
	}
</style>
