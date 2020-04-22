<script>
</script>

<style lang="scss">
	.button {
	  display: flex;
	  align-items: center;
	  justify-content: center;

	  cursor: pointer;
	}

	.button svg {
	  height: 55px;
	  width: 150px;
	  fill: none;
	  stroke-width: 5;
	}
	.button svg .o1 {
	  stroke: rgba(#ffb341, 0.7);
	  fill: #ffa114;
	  transition: all 1s ease-in-out;
	}

	.button svg .o2 {
	  stroke: white;
	  stroke-dasharray: 20 420;
	  stroke-dashoffset: 20;
	  transition: all 1s ease-in-out;
	}

	span {
	  position: absolute;
	  margin: auto 0;
	  text-transform: uppercase;
	  letter-spacing: 3px;
	}

	.button:hover .o1 {
	  fill: rgba(#cc8110, 0.3);
	}
	.button:hover .o2 {
	  stroke-dashoffset: -420;
	}
</style>

<div class="button">
		<span>Hover Me</span>
		<svg>
		<polyline class="o1" points="0 0, 150 0, 150 55, 0 55, 0 0"></polyline>
		<polyline class="o2" points="0 0, 150 0, 150 55, 0 55, 0 0"></polyline>
	</svg>
</div>
