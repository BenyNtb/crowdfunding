<template>
  <div class="border-2 border-gray-300 rounded-lg flex py-6" @click="handleModalSelect(modal.id);">
    <div class="w-16 flex justify-center">
      <input
        type="radio"
        class="bg-gray-100 border-0 mt-0.5 ring-2 ring-dark-cyan caret-dark-cyan text-dark-cyan"
        name="inputRadioThanksModal"
        v-model="modalSelected"
        :value="modal.id"
        @click="handleModalSelect(modal.id)"
      />
    </div>
    <div class="w-full pr-4">
      <div class="w-full mb-6 flex items-center justify-between">
        <div class="flex justify-between space-x-4">
          <h3 class="text-black hover:text-dark-cyan font-bold">{{ modal.name }}</h3>
          <h3 class="text-dark-cyan font-semibold">Pledge ${{ modal.min_price }} or more</h3>
        </div>
        <div class="flex items-center">
          <span class="font-bold text-black">{{ modal.left }}</span>
          <span class="text-base text-dark-gray ml-2.5">left</span>
        </div>
      </div>
      <p class="text-xs text-dark-gray">{{ modal.description }}</p>
      <!-- form -->
      <div class="w-full py-4" v-show="modal.id == modalSelected">
        <hr class="w-full bg-gray-600" />
        <div class="flex w-full justify-between items-center pt-4">
          <p class="text-gray-600">Enter your pledge</p>
          <input
            type="number"
            v-model="amount"
            class="rounded-full border-2 border-gray-600 w-32 text-dark-cyan"
          />
          <button class="px-6 py-2 bg-dark-cyan rounded-full" @click="submitDataModal">Submit</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    submitDataModal () {
      let modal = {modal:{...this.modal}, amount: this.amount};
      modal.modal.left--;
      this.$emit('submitDataModal', modal)
    },
  },
  props: {
    modal: { type: Object },
    modalSelected: { type: Number },
    handleModalSelect: { type: Function },
  },
  data () {
    return {
      amount: this.modal.min_price,
    }
  },
}
</script>

<style>
</style>