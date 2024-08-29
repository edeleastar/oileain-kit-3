<script>
  import "../app.css";
</script>

<div class="grid h-screen grid-rows-[auto_1fr_auto]">
  <!-- Header -->
  <header class="bg-red-500 p-4">(header)</header>
  <!-- Main -->
  <slot></slot>
  <!-- Footer -->
  <footer class="bg-blue-500 p-4">(footer)</footer>
</div>
