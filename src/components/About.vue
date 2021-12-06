<template>
  <div class="px-8 py-14 bg-white rounded-lg border-1">
    <h2 class="font-bold text-black mb-9 text-lg">About this project</h2>
    <p class="text-dark-gray text-justify">
      The Mastercraft Bamboo Monitor Riser is a sturdy and stylish platform that elevates your scrren to a more comfortable viewing height. Placing your monitor at eye level has the potential to improve your posture and make you more comfortable white at work, helping you stay focused on the task at hand.
      <br />
      <br />Featuring artisan craftsmanship, the simplicity of design creates extra desk space below your computer to allow notepads, pen, and USB sticks to be stored under the stand.
    </p>
    <div class="flex flex-col w-full justify-center space-y-7">
      <Modal v-for="modal in data" :key="'modal' + modal.id" :modal="modal" :handleOpenRewards="handleOpenRewards" />
    </div>
  </div>
</template>

<script>
import Modal from "./Modal.vue";
export default {
  components: { Modal },
  props: {
    data: {
      type: Object,
    },
    handleOpenRewards: { type: Function}
  }
}
</script>

<style>
</style>