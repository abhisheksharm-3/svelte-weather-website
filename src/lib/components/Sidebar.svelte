<script lang="ts">
  import Button from "./ui/button/button.svelte";
  import { CloudSunRain, List, Map, SlidersHorizontal } from "lucide-svelte";
</script>

<aside
  class="bg-gray-700 h-[85vh] rounded-3xl py-8 flex flex-col items-center gap-10"
>
  <img
    src="/icons/sun.png"
    alt="logo"
    class="w-[3%] animate-spin-slow absolute"
  />

  <a
    class="mt-32 flex flex-col items-center justify-center group text-gray-400 cursor-pointer"
    href="/app/forecast"
  >
    <CloudSunRain
      class="group-hover:text-white ease-in-out duration-500 "
    /><Button
      variant="ghost"
      class="group-hover:text-white group-hover:bg-transparent ease-in-out duration-500 "
    >
      Weather</Button
    >
  </a>
  <a class="flex flex-col items-center justify-center group text-gray-400 cursor-pointer" href="/app/cities">
    <List class="group-hover:text-white ease-in-out duration-500 " /><Button
      variant="ghost"
      class="group-hover:text-white group-hover:bg-transparent ease-in-out duration-500 "
      
    >
      Cities</Button
    >
  </a>
  <a class="flex flex-col items-center justify-center group text-gray-400 cursor-pointer" href="/app/map">
    <Map class="group-hover:text-white ease-in-out duration-500 " /><Button
      variant="ghost"
      class="group-hover:text-white group-hover:bg-transparent ease-in-out duration-500 "
    >
      Map</Button
    >
  </a>
  <a class="flex flex-col items-center justify-center group text-gray-400 cursor-pointer" href="/app/settings">
    <SlidersHorizontal
      class="group-hover:text-white ease-in-out duration-500 "
    /><Button
      variant="ghost"
      class="group-hover:text-white group-hover:bg-transparent ease-in-out duration-500 "
      
    >
      Settings</Button
    >
  </a>
</aside>
