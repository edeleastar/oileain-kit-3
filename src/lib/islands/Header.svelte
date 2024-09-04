<script lang="ts">
  import { AppBar } from "@skeletonlabs/skeleton-svelte";
  import Paperclip from "lucide-svelte/icons/paperclip";
  import LocateFixed from "lucide-svelte/icons/locate-fixed";
  import DraftingCompass from "lucide-svelte/icons/drafting-compass";
  import MapPinned from "lucide-svelte/icons/map-pinned";
</script>

<!-- <AppBar background="bg-surface-100-800-token" classes="h-28 border-b-[1px] border-surface-200 dark:border-surface-700"> -->
<AppBar background="bg-surface-100-800-token" headlineClasses="sm:hidden" centerClasses="hidden sm:block border-b-[1px] border-surface-200 dark:border-surface-700">
  {#snippet lead()}
    <p class="h3">Oileain: Islands of Ireland</p>
  {/snippet}
  {#snippet trail()}
    <a href="/"><MapPinned size={40} /> </a>
    <a href="/explorer"><LocateFixed size={40} /></a>
    <a href="/navigator/Great-Saltee-Island"><DraftingCompass size={40} /></a>
  {/snippet}
</AppBar>
