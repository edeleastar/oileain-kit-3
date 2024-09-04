<script lang="ts">
  import type { Island } from "../model/oileain-types";
  import { sharedIsland } from "$lib/model/shared-state";
  export let island: Island;
</script>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">GPS-compatible</caption>
  <tbody>
    <tr>
      <td>Latitude</td>
      <td>{island.coordinates.geo.lat}</td>
    </tr>
    <tr>
      <td>Longitude</td>
      <td>{island.coordinates.geo.long}</td>
    </tr>
  </tbody>
</table>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">Transverse Mercator</caption>
  <tbody>
    <tr>
      <td>Eastings</td>
      <td>{island.coordinates.tmcGrid.eastings}</td>
    </tr>
    <tr>
      <td>Northings</td>
      <td>{island.coordinates.fullIrishGrid.northings}</td>
    </tr>
  </tbody>
</table>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">Full Irish Grid</caption>
  <tbody>
    <tr>
      <td>Eastings</td>
      <td>{island.coordinates.fullIrishGrid.eastings}</td>
    </tr>
    <tr>
      <td>Northings</td>
      <td>{island.coordinates.fullIrishGrid.northings}</td>
    </tr>
  </tbody>
</table>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">Irish Grid</caption>
  <tbody>
    <tr>
      <td>Sheet</td>
      <td>{island.coordinates.irishGrid.sheet}</td>
    </tr>
    <tr>
      <td>Eastings</td>
      <td>{island.coordinates.irishGrid.eastings}</td>
    </tr>
    <tr>
      <td>Norhtings</td>
      <td>{island.coordinates.irishGrid.northings}</td>
    </tr>
  </tbody>
</table>
