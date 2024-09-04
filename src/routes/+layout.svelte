<script lang="ts">
  import "../app.css";
  import { onMount } from "svelte";
  import Header from "$lib/islands/Header.svelte";
  import SideBar from "$lib/islands/SideBar.svelte";
  import { oileainService } from "../lib/model/oileain-service";
  import type { IslandGroup } from "../lib/model/oileain-types";

  let { children } = $props();

  let allCoasts: IslandGroup[] = $state([]);
  onMount(async () => {
    allCoasts = await oileainService.getCoasts();
  });
</script>

<Header />

<div class="flex min-h-full flex-col">
  <div class="max-w-8xl mx-auto w-full grow lg:flex xl:px-2">
    <div class="flex-1 xl:flex">
      <div class="px-4 py-6 sm:px-6 lg:pl-8 xl:flex-1 xl:pl-6">
        <!-- <p class="h-[512px] bg-purple-500 p-4">Paragraph 3</p> -->
        {@render children()}
      </div>
    </div>
    <div class="shrink-0 border-t border-gray-200 px-4 py-6 sm:px-6 lg:w-72 lg:border-l lg:border-t-0 lg:pr-8 xl:pr-6">
      <SideBar {allCoasts} />
    </div>
  </div>
</div>
