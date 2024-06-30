<script>
  import "remixicon/fonts/remixicon.css";
  const forecast = [
    { time: "6:00 AM", icon: "ri-cloud-line", temperature: 25 },
    { time: "9:00 AM", icon: "ri-sun-cloudy-line", temperature: 28 },
    { time: "12:00 PM", icon: "ri-sun-line", temperature: 33 },
    { time: "3:00 PM", icon: "ri-sun-line", temperature: 34 },
    { time: "6:00 PM", icon: "ri-sun-line", temperature: 32 },
    { time: "9:00 PM", icon: "ri-sun-cloudy-line", temperature: 30 },
  ];
  const dailyForecast = [
    {
      day: "Today",
      icon: "ri-sun-line",
      description: "Sunny",
      high: 36,
      low: 22,
    },
    {
      day: "Tue",
      icon: "ri-sun-line",
      description: "Sunny",
      high: 37,
      low: 21,
    },
    {
      day: "Wed",
      icon: "ri-sun-line",
      description: "Sunny",
      high: 37,
      low: 21,
    },
    {
      day: "Thu",
      icon: "ri-cloud-line",
      description: "Cloudy",
      high: 37,
      low: 21,
    },
    {
      day: "Fri",
      icon: "ri-cloud-line",
      description: "Cloudy",
      high: 37,
      low: 21,
    },
    {
      day: "Sat",
      icon: "ri-rainy-line",
      description: "Rainy",
      high: 37,
      low: 21,
    },
    {
      day: "Sun",
      icon: "ri-sun-line",
      description: "Sunny",
      high: 37,
      low: 21,
    },
  ];
</script>

<svelte:head>
  <title>Forecast</title>
  <meta name="description" content="Weather Website" />
</svelte:head>
<div class="container">
  <div class="flex w-full h-full gap-4">
    <div class="w-2/3 flex flex-col gap-3">
      <div class="flex justify-between py-20 items-start">
        <div class="flex flex-col justify-between">
          <div class="flex flex-col gap-2">
            <h1 class="font-bold text-5xl">Madrid</h1>
            <span class="text-gray-400">Chances of rain: 0%</span>
          </div>
          <h1 class="font-bold text-7xl">31&deg;</h1>
        </div>
        <div class="flex items-center justify-center">
          <img
            src="/icons/sun.png"
            alt="weather illustration"
            class="w-[60%]"
          />
        </div>
      </div>
      <div class="bg-gray-700 h-full w-full rounded-3xl container py-6">
        <h3 class="text-gray-400 uppercase text-sm">Today's Forecast</h3>
        <div class="flex p-4 text-white rounded-lg">
          {#each forecast as { time, icon, temperature }, index}
            <div class="text-center flex-1">
              <div>{time}</div>
              <div class="text-2xl my-2">
                <i class={icon}></i>
              </div>
              <div class="text-xl">{temperature}°</div>
            </div>
            {#if index < forecast.length - 1}
              <div class="border-l border-gray-600 mx-2"></div>
            {/if}
          {/each}
        </div>
      </div>
      <div class="bg-gray-700 h-full w-full rounded-3xl container py-6">
        <h3 class="text-gray-400 uppercase text-sm">Air Conditions</h3>
        <div class="grid grid-cols-2 gap-4">
          <div class="flex items-center">
            <i class="ri-temp-hot-line text-2xl mr-2"></i>
            <div>Real Feel: 28&deg;</div>
          </div>
          <div class="flex items-center">
            <i class="ri-windy-line text-2xl mr-2"></i>
            <div>Wind: 10 km/h</div>
          </div>
          <div class="flex items-center">
            <i class="ri-umbrella-line text-2xl mr-2"></i>
            <div>Chances of Rain: 0%</div>
          </div>
          <div class="flex items-center">
            <i class="ri-sun-fill text-2xl mr-2"></i>
            <div>UV Index: 5</div>
          </div>
        </div>
      </div>
    </div>
    <div class="w-1/3 container ">
      <div class="bg-gray-700 p-10 text-white rounded-3xl h-full flex flex-col gap-3">
        <h3 class="text-gray-400 uppercase text-sm">7-Day Forecast</h3>
        <div class="h-full flex-1 flex flex-col justify-between">
          {#each dailyForecast as { day, icon, description, high, low }}
            <div class="flex items-center justify-between py-2 border-b border-gray-600 last:border-b-0">
              <div class="flex items-center space-x-12">
                <div class="text-sm">{day}</div>
                <i class="{icon} text-2xl"></i>
                <div class="text-sm">{description}</div>
              </div>
              <div class="text-sm">{high}/{low}</div>
            </div>
          {/each}
        </div>
      </div>
    </div>
  </div>
</div>
