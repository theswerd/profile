<script>
  export let backgroundColor;
</script>

<style>
  section {
    height: 100%;
    min-width: 100vw;

    display: flex;
    background-color: var(--background-color);

    scroll-snap-align: start;
  }
</style>

<section style="--background-color: {backgroundColor}">
  <slot />
</section>
