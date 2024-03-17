<script>
  export let white = false;
</script>

<h2 class={$$props.class} class:white={white}>
  <slot />
</h2>

<style>
  h2 {
    font-size: 1.75rem;
    font-weight: 400;
  }

  .white {
    color: #fff;
  }
</style>
