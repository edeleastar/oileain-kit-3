<script lang="ts">
  import { sharedIsland } from "$lib/model/shared-state";
  import IslandLocation from "./IslandLocation.svelte";
</script>

<IslandLocation title="GPS Compatible" XName={"Latitude"} YName={"Longitude"} X={sharedIsland?.value?.coordinates.geo.lat} Y={sharedIsland?.value?.coordinates.geo.long} />
<IslandLocation
  title="Transverse Mercator"
  XName={"Eastings"}
  YName={"Northings"}
  X={sharedIsland?.value?.coordinates.tmcGrid.eastings}
  Y={sharedIsland?.value?.coordinates.tmcGrid.northings}
/>
<IslandLocation
  title="Full Irish Grid"
  XName={"Eastings"}
  YName={"Northings"}
  X={sharedIsland?.value?.coordinates.fullIrishGrid.eastings}
  Y={sharedIsland?.value?.coordinates.fullIrishGrid.northings}
/>

<IslandLocation
  title="Irish Grid"
  XName={"Sheet"}
  YName={"Eastings"}
  ZName={"Northings"}
  X={sharedIsland?.value?.coordinates.irishGrid.sheet}
  Y={sharedIsland?.value?.coordinates.irishGrid.eastings}
  Z={sharedIsland?.value?.coordinates.irishGrid.northings}
/>
