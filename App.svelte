<script>
  import Menu from "./components/Menu.svelte";
  import Toggle from "./components/Toggle.svelte";
  import Viewport from "./components/Viewport.svelte";
  import Button from "./components/Button.svelte";

  const menuItems = [{ label: "Reaper" }, { label: "Ninja" }];

  let checked = true;
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
    margin-left: 5rem;
  }
</style>

<main>
  <Button />
	<h1>Hello CodeSandbox</h1>
	<h2>Start editing to see some magic happen!</h2>
	<Menu items={menuItems}/>
  <Toggle bind:checked={checked} />
</main>