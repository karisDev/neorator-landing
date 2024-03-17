<script>
  export let column = false;
  export let align = "start";
  export let justify = "start";
  export let gap = 0;
  export let wrap = false;
</script>

<div class="{column ? "column" : ""} {$$props.class}" style="align-items: {align}; justify-content: {justify}; gap: {gap}px; flex-wrap: {wrap ? "wrap" : "nowrap"};">
  <slot />
</div>

<style>
  div {
    display: flex;
  }

  .column {
    flex-direction: column;
  }
</style>
