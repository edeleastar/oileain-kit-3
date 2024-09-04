<script lang="ts">
  import IslandCoordinates from "$lib/islands/IslandCoordinates.svelte";
  import IslandDescription from "$lib/islands/IslandDescription.svelte";
  import IslandMap from "$lib/maps/IslandMap.svelte";
</script>

<div class="grid grid-cols-2 gap-4">
  <div>
    <IslandMap zoom={12} height={40} />
    <div class="align-center grid w-72 rounded-lg shadow-xl">
      <IslandCoordinates />
    </div>
  </div>
  <div class="p-6"><IslandDescription /></div>
</div>
