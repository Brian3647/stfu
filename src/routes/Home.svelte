<script lang="ts">
  import { fly } from "svelte/transition";

  let visible = false,
    extra_visible = false;

  setTimeout(() => {
    visible = true;
  }, 400);

  setTimeout(() => {
    extra_visible = true;
  }, 400);
</script>

{#if visible}
  <div class="home" transition:fly={{ duration: 1200, y: 300 }}>
    <div class="center">
      <h1 class="title">Shut up.</h1>
      <p class="subtitle">No more text needed. Just stop talking.</p>
    </div>
  </div>
{/if}

<style lang="scss">
  @import "../styles/home.scss";
</style>
