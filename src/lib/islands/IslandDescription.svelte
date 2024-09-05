<script lang="ts">
  import { sharedIsland } from "$lib/model/shared-state";
</script>

<section class="m-2 box-border border-4 p-4">
  {#if sharedIsland.value}
    {@html sharedIsland?.value?.description}
  {:else}{/if}
</section>
