<script lang="ts">
  import type { PageData } from "./$types";
  export let data: PageData;
  import IslandDescription from "$lib/islands/IslandDescription.svelte";
  import CoastalMap from "$lib/maps/CoastalMap.svelte";
  import IslandMap from "$lib/maps/IslandMap.svelte";
  import IslandLocation from "$lib/islands/IslandLocation.svelte";
  import { sharedIsland } from "$lib/model/shared-state";
</script>

<div class="grid grid-cols-2 gap-4">
  <div>
    <CoastalMap zoom={7} height={60} markerLayers={data.markerLayers} />
    <div>
      <IslandLocation title="GPS Compatible" XName={"Latitude"} YName={"Longitude"} X={sharedIsland?.value?.coordinates.geo.lat} Y={sharedIsland?.value?.coordinates.geo.long} />
    </div>
  </div>
  <div>
    <IslandMap zoom={16} height={40} />
    <IslandDescription />
  </div>
</div>
