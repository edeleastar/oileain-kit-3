<script lang="ts">
  type Props = {
    title: string;
    XName: string;
    YName: string;
    ZName?: string;
    X?: number | string;
    Y?: number;
    Z?: number;
  };

  let { title, XName, YName, ZName, X, Y, Z }: Props = $props();
</script>

<div class="m-2 box-border border-4 p-2">
  <div class="p-4">
    <table class="table table-fixed caption-bottom">
      <caption class="pt-4">{title}</caption>
      <tbody>
        <tr>
          <td>{XName}</td>
          <td>{X}</td>
        </tr>
        <tr>
          <td>{YName}</td>
          <td>{Y}</td>
        </tr>

        {#if ZName}
          <tr>
            <td>{ZName}</td>
            <td>{Z}</td>
          </tr>
        {/if}
      </tbody>
    </table>
  </div>
</div>
