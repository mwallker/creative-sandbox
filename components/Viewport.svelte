<script>
  import { onMount } from "svelte";

  let worldAngle = { x: 0, y: 0 };
  let world;

  function handleMove(event) {
    const { touches } = event;
    const { clientX, clientY } = touches ? touches[0] : event;
    const { innerWidth, innerHeight } = window;

    worldAngle = {
      x: -(0.5 - clientY / innerHeight) * 180 * 0.8,
      y: (0.5 - clientX / innerWidth) * 180 * 0.8
    };
  }
</script>

<style>
  .viewport {
    bottom: 0;
    left: 0;
    overflow: hidden;
    perspective: 500px;
    position: absolute;
    right: 0;
    top: 0;
  }

  .world {
    height: 512px;
    left: 50%;
    margin-left: -256px;
    margin-top: -256px;
    position: absolute;
    top: 50%;
    transform-style: preserve-3d;
    width: 512px;
    background: #12908e;
  }
</style>

<div class="viewport" bind:this={world} on:mousemove={handleMove} on:touchmove={handleMove}>
	<div class="world" style="transform: translateZ(100px) rotateX({worldAngle.x}deg) rotateY({worldAngle.y}deg)"></div>
</div>
