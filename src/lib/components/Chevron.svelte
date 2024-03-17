<script lang="ts">
  let width = 15;
  export { width as size };
  export let direction: "up" | "down" | "left" | "right" = "down";

  $: rotation = {
    right: 0,
    down: 90,
    left: 180,
    up: 270,
  }[direction];
</script>

<svg
  {width}
  style="--rotation: {rotation}deg; min-width: {width}px;"
  class={$$props.class}
  viewBox="0 0 20 20"
  fill="none"
  xmlns="http://www.w3.org/2000/svg"
>
  <path d="M7.5 15L12.5 10L7.5 5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
</svg>

<style>
  svg {
    transform: rotate(var(--rotation));
  }
</style>
