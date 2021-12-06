<template>
  <div class="w-full flex flex-col items-center border-1 mt-52 pb-12 rounded-lg bg-white" :class="bookmarked == false || bookmarked == null && 'cursor-pointer'">
    <h1 class="text-black font-black text-2xl mb-3.5">Mastercraft Bamboo Monitor Riser</h1>
    <p class="text-gray-500">A beautiful & handcrafted monitor stand neck and eye strain.</p>
    <div class="w-full px-16 mt-10 flex justify-between">
      <button class="py-4 px-9 text-white font-bold bg-dark-cyan hover:bg-moderate-cyan rounded-full" @click="handleOpenRewards">Back this project</button>
      <div class="bg-gray-200 rounded-full flex items-center justify-between">
        <svg v-show="bookmarked == false || bookmarked == null"  width="56" height="56" xmlns="http://www.w3.org/2000/svg"><g fill="#ff00ff" fill-rule="evenodd"><circle fill="#147b74" cx="28" cy="28" r="28"/><path fill="currentColor" d="M23 19v18l5-5.058L33 37V19z"/></g></svg>
        <svg v-show="bookmarked == true" width="56" height="56" xmlns="http://www.w3.org/2000/svg"><g fill="#222" fill-rule="evenodd"><circle fill="#2F2F2F" cx="28" cy="28" r="28"/><path fill="#999" d="M23 19v18l5-5.058L33 37V19z"/></g></svg>
        <span class="ml-6 mr-8 font-bold text-dark-cyan" :class="bookmarked == true && 'text-gray-600'">Bookmark</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    openRewards: { type: Boolean},
    handleOpenRewards: {type: Function},
  },
  data () {
    return {
      bookmarked: false,
    }
  }
}
</script>

<style>

</style>