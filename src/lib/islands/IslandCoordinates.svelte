<script lang="ts">
  import { sharedIsland } from "$lib/model/shared-state";
</script>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">GPS-compatible</caption>
  <tbody>
    <tr>
      <td>Latitude</td>
      <td>{sharedIsland?.value?.coordinates.geo.lat}</td>
    </tr>
    <tr>
      <td>Longitude</td>
      <td>{sharedIsland?.value?.coordinates.geo.long}</td>
    </tr>
  </tbody>
</table>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">Transverse Mercator</caption>
  <tbody>
    <tr>
      <td>Eastings</td>
      <td>{sharedIsland?.value?.coordinates.tmcGrid.eastings}</td>
    </tr>
    <tr>
      <td>Northings</td>
      <td>{sharedIsland?.value?.coordinates.fullIrishGrid.northings}</td>
    </tr>
  </tbody>
</table>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">Full Irish Grid</caption>
  <tbody>
    <tr>
      <td>Eastings</td>
      <td>{sharedIsland?.value?.coordinates.fullIrishGrid.eastings}</td>
    </tr>
    <tr>
      <td>Northings</td>
      <td>{sharedIsland?.value?.coordinates.fullIrishGrid.northings}</td>
    </tr>
  </tbody>
</table>

<table class="table table-fixed caption-top">
  <caption class="h3 pt-8">Irish Grid</caption>
  <tbody>
    <tr>
      <td>Sheet</td>
      <td>{sharedIsland?.value?.coordinates.irishGrid.sheet}</td>
    </tr>
    <tr>
      <td>Eastings</td>
      <td>{sharedIsland?.value?.coordinates.irishGrid.eastings}</td>
    </tr>
    <tr>
      <td>Norhtings</td>
      <td>{sharedIsland?.value?.coordinates.irishGrid.northings}</td>
    </tr>
  </tbody>
</table>
