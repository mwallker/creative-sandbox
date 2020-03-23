<script>
	export let items = [];
</script>

<style>
	:root {
	  font-size: 16px;
	  font-family: "Bellota Text", cursive;

	  --bgPrimary: rgb(70, 70, 70);
	  --bgSecondary: rgb(0, 175, 137);

	  --transitionSpeed: 500ms;
	}

	.menu-container {
	  position: fixed;
	  left: 0;
	  background-color: var(--bgPrimary);
	  transition: width var(--transitionSpeed);
	  font-family: "Bellota Text", cursive;
	}

	.menu {
	  list-style: none;
	  padding: 0;
	  margin: 0;
	  display: flex;
	  align-items: center;
	  height: 100%;
	}

	.menu-item {
	  width: 100%;
	  display: flex;
	  overflow: hidden;
	}

	.menu-item a {
	  display: flex;
	  width: 100%;
	  align-items: center;
	  padding: 1.5rem;
	  color: var(--bgSecondary);
	  text-decoration: none;
	  filter: grayscale(100%) opacity(0.7);
	  transition: var(--transitionSpeed);
	}

	.menu-item a:hover {
	  filter: grayscale(0%) opacity(1);
	  color: var(--bgSecondary);
	  background-color: black;
	}

	.text {
	  display: none;
	  margin-left: 1rem;
	}

	.icon svg {
	  width: 2rem;
	}

	@media screen and (min-width: 600px) {
	  .menu-container {
	    width: 5rem;
	    height: 100vh;
	    top: 0;
	  }

	  .menu-container:hover {
	    width: 16rem;
	  }

	  .menu-container:hover .text {
	    display: inline;
	  }

	  .menu {
	    flex-direction: column;
	  }
	}

	@media screen and (max-width: 600px) {
	  .menu-container {
	    width: 100vw;
	    height: 5rem;
	    bottom: 0;
	  }

	  .menu {
	    flex-direction: row;
	  }

	  .menu-item a {
	    justify-content: center;
	  }
	}
</style>

<nav class="menu-container">
	<ul class="menu">
		{#each items as item}
			<li class="menu-item">
				<a href>
					<span class="icon">
						<svg viewBox="0 0 512 512">
							<use href="#Reaper" />
						</svg>
					</span>
					<span class="text">{item.label}</span>
				</a>
			</li>
		{/each}
	</ul>
</nav>