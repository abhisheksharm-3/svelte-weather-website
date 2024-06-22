<script>
  import Sidebar from "$lib/components/Sidebar.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
</script>

<div class="p-10 flex gap-10 w-screen">
  <div class="w-1/12"><Sidebar /></div>
  <div class="flex flex-col w-11/12"><Navbar /><slot></slot></div>
</div>
