<script>
  import "./globals.css"
</script>

<div class="app">
  <slot />
</div>

<style>
  .app {
    height: 100dvh;
    width: 100dvw;

    color: var(--color-text);
    background-color: var(--color-background-primary);
  }
</style>