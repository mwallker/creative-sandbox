<script>
  export let id = "fsdf";
  export let checked;
</script>

<style>
  :root {
    --teal-and-orange-1: #c4421a;
    --teal-and-orange-2: #f98f45;
    --teal-and-orange-3: #97cecc;
    --teal-and-orange-4: #12908e;
    --teal-and-orange-5: #16594a;
  }

  span.toggle-container {
    font-size: 0;
    display: inline-block;
  }

  input.toggle:checked ~ label.toggle-label {
    background-color: rgb(3, 102, 69);
    border-radius: 50%;
  }

  input.toggle {
    display: none;
  }

  label.toggle-label {
    background-color: black;
    display: inline-block;
    min-height: 2rem;
    min-width: 2rem;
    transition: 0.2s;
  }
</style>

<span class="toggle-container">
  <input type="checkbox" bind:checked id={id} class="toggle toggle-flat">
  <label for={id} class="toggle-label"></label>
</span>
