<script>
  import Button from "$lib/components/ui/button/button.svelte";
</script>

<svelte:head>
  <title>METEOHUB</title>
  <meta name="description" content="Weather Website" />
</svelte:head>

<div class="w-screen h-screen flex items-center justify-around gap-12 lg:gap-0 flex-col lg:flex-row container py-20">
  <div class="bg-gray-700 w-full lg:w-1/2 h-full rounded-3xl flex items-center justify-center"><img src="/icons/planet-12970_256.gif" alt="planet earth" class="w-[60%]" /></div>
  <div class="flex flex-col items-center justify-center gap-10">
	<img alt="Sun Logo" src="/icons/sun.png" class="w-[20%] animate-spin-slow"/>
    <div class="flex flex-col gap-4 items-center justify-center">
      <h2 class="text-6xl font-bold">MeteoHub</h2>
      <h3 class="text-gray-400 text-lg">The Weather App</h3>
    </div>
    <Button
      class="rounded-3xl bg-[#0095ff] text-white ease-in-out duration-500 hover:bg-blue-600"
      >Get Started</Button
    >
  </div>
</div>
