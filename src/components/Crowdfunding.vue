<template>
  <div class="crowdfunding-container flex flex-col justify-center space-y-6">
    <Header :openRewards="openRewards" :handleOpenRewards="handleOpenRewards" />
    <Backers :data="{ ...crowdfunding.statistics }" />
    <About
      :openRewards="openRewards"
      :data="{ ...crowdfunding.mode }"
      :handleOpenRewards="handleOpenRewards"
    />
    <Thanks
      @closeThanks="handleOpenRewards"
      v-show="openRewards == true"
      :data="{ ...crowdfunding.mode }"
      :modalSelected="modalSelected"
      :modalSelect="modalSelect"
      @submitDataModal="submitDataModal"
    />
  </div>
</template>

<script>
import Backers from "./Backers.vue";
import Header from "./Header.vue";
import About from "./About.vue";
import Thanks from "./Thanks.vue";
export default {
  name: "Crowdfunding",
  components: {
    Header, Backers, About
    , Thanks
  },
  methods: {
    handleOpenRewards () {
      return this.openRewards = !this.openRewards;
    },
    modalSelect (modal) {
      this.modalSelected = modal
    },
    submitDataModal (data) {
      let mode = [...this.crowdfunding.mode].map(e => e.id == data.modal.id ? data.modal : e);
      this.crowdfunding.mode = mode;
      this.crowdfunding.statistics.backed.current = this.crowdfunding.statistics.backed.current + data.amount;
      this.crowdfunding.statistics.backers = this.crowdfunding.statistics.backers - 1;
    }
  },
  data () {
    return {
      openRewards: false,
      modalSelected: null,
      crowdfunding: {
        statistics: {
          backed: {
            current: 89914,
            total: 100000,
          },
          backers: 5007,
          days_left: 56,
        },
        mode: [
          {
            id: 1,
            name: 'Bamboo Stand',
            description: "You get an ergonomic stand made of natural bamboo. You've helped us launch our promotional campaign, and you'il be added to a special Backer member list.",
            left: 101,
            min_price: 25,
          },
          {
            id: 2,
            name: 'Black Edition Stand',
            description: "You get a Black Special Edition computer stand and a personnal thank you. You'il be added to our Backed member list. Shipping is included.",
            left: 64,
            min_price: 75,
          },
          {
            id: 3,
            name: "Mahogany Special Edition",
            description: "You get two Special Edition Mahogany stands, a Backer T-Shirt, and a personal thank you. You'il be added to our Backer member list. Shipping is incuded.",
            left: 1,
            min_price: 200,
          },
        ]
      },
    }
  }
}
</script>

<style scoped>

</style>