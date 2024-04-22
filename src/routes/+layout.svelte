<script>
  import "./globals.css"
</script>

<div class="app">
  <slot />
</div>

<style>
  .app {
    height: 100%;
    width: 100%;

    border: 1px solid transparent;

    color: var(--color-text);
    background-color: var(--color-background-primary);
  }
</style>