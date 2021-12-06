<template>
  <div class="p-12 bg-white border-1 rounded-lg">
    <div class="flex items-center w-full text-black">
      <div class="w-1/3 flex flex-col">
        <span class="font-bold text-2xl">${{ data.backed.current }}</span>
        <span class="text-base text-dark-gray">of {{ data.backed.total }} backed</span>
      </div>
      <div class="w-1/3 flex flex-col justify-center items-center border-l-2 border-r-2">
        <span class="font-bold text-2xl">{{ data.backers }}</span>
        <span class="text-base text-dark-gray">total backers</span>
      </div>
      <div class="w-1/3 flex flex-col pl-16">
        <span class="font-bold text-2xl">{{ data.days_left }}</span>
        <span class="text-base text-dark-gray">days left</span>
      </div>
    </div>
    <!-- Progress bar -->
    <div class="rounded-full h-3.5 mt-10 bg-gray-200">
      <div class="rounded-full h-full bg-dark-cyan" :style="{width: data.backed.current / data.backed.total * 100 + '%'}"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Backers',
  props: {
    data: {
      type: Object,
    },
  }
}
</script>

<style>
</style>