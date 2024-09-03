<script lang="ts">
  import "../app.css";
  import { AppBar } from "@skeletonlabs/skeleton-svelte";
  import ArrowLeft from "lucide-svelte/icons/arrow-left";
  import Paperclip from "lucide-svelte/icons/paperclip";
  import Calendar from "lucide-svelte/icons/calendar";
  import CircleUser from "lucide-svelte/icons/circle-user";
  let { children } = $props();
</script>

<AppBar background="bg-surface-100-800-token" classes="h-20 justify-center border-b-[1px] border-surface-200 dark:border-surface-700">
  {#snippet lead()}
    <ArrowLeft size={24} />
  {/snippet}
  {#snippet trail()}
    <Paperclip size={20} />
    <Calendar size={20} />
    <CircleUser size={20} />
  {/snippet}
  {#snippet headline()}
    <h2 class="h5">Oileain: Islands of Ireland</h2>
  {/snippet}
</AppBar>

{@render children()}
