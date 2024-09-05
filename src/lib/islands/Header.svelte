<script lang="ts">
  import { AppBar } from "@skeletonlabs/skeleton-svelte";
  import Icon from "@iconify/svelte";
</script>

<AppBar background="bg-surface-100-800-token" headlineClasses="sm:hidden" centerClasses="hidden sm:block  border-surface-200 dark:border-surface-700">
  {#snippet lead()}
    <a target="_blank" href="https://github.com/edeleastar/oileain-kit-3">
      <div class="flex flex-col items-center">
        <div>
          <Icon icon="logos:github-octocat" width="60" />
        </div>
        <div>
          <h6>Source Repo</h6>
        </div>
      </div>
    </a>
  {/snippet}
  <div class="flex place-content-center p-4">
    <p class="h3">Oileain: Islands of Ireland</p>
  </div>
  {#snippet trail()}
    <div class="flex place-content-center gap-14 p-4">
      <a href="/" class="column">
        <Icon icon="mdi:compass-rose" width="64" />
      </a>
      <a href="/explorer" class="column">
        <Icon icon="ph:compass-tool-duotone" width="64" />
      </a>
      <a href="/navigator/Great-Saltee-Island" class="column">
        <Icon icon="mdi:ruler-square-compass" width="64" />
      </a>
    </div>
  {/snippet}
</AppBar>
