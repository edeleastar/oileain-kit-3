<script lang="ts">
  import { onMount } from "svelte";
  import { page } from "$app/stores";
  import IslandDescription from "$lib/islands/IslandDescription.svelte";
  import type { PageData } from "./$types";
  import IslandMap from "$lib/maps/IslandMap.svelte";
  import CoastalMap from "$lib/maps/CoastalMap.svelte";
  import { sharedIsland, sharedMarker } from "$lib/model/shared-state";
  export let data: PageData;

  page.subscribe((path) => {
    sharedMarker.value = data.marker;
    sharedIsland.value = data.island;
  });

  onMount(async () => {
    sharedMarker.value = data.marker;
    sharedIsland.value = data.island;
  });
</script>

<div class="grid grid-cols-2 gap-4">
  <div>
    <IslandMap zoom={14} height={40} />
  </div>
  <div style="height: 45vh; overflow-y: auto">
    <IslandDescription />
  </div>
</div>
<div class="grid grid-cols-2 gap-4">
  <div>
    <IslandMap defautLayer={"Satellite"} zoom={14} height={40} />
  </div>
  <div>
    <CoastalMap zoom={9} height={40} location={sharedMarker?.value?.location} markerLayers={data.markerLayers} />
  </div>
</div>
