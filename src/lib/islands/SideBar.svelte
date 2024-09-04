<script lang="ts">
  import { Accordion } from "@skeletonlabs/skeleton-svelte";
  import MapPinned from "lucide-svelte/icons/map-pinned";
  import type { IslandGroup } from "../model/oileain-types";

  type Props = {
    allCoasts: IslandGroup[];
  };
  let { allCoasts = [] }: Props = $props();
</script>

<Accordion collapsible>
  {#each allCoasts as coast}
    <Accordion.Item value={coast.title}>
      {#snippet lead()}<MapPinned size={24} />{/snippet}
      {#snippet control()}
        {coast.title}
      {/snippet}
      {#snippet panel()}
        {#each coast.pois as island}
          <a class="anchor" href="/navigator/{island.safeName}"> {@html island.name}</a>
        {/each}
      {/snippet}
    </Accordion.Item>
    <hr class="hr" />
  {/each}
</Accordion>
