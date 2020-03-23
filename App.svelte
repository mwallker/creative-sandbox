<script>
  import Button from "./Button.svelte";
  import Menu from "./components/Menu.svelte";

  const menuItems = [{ label: "Reaper" }, { label: "Ninja" }];
</script>

<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>

<main>
	<h1>Hello CodeSandbox</h1>
	<h2>Start editing to see some magic happen!</h2>
	<Menu items={menuItems}/>
</main>