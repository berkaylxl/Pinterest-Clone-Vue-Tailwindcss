<template>
  <div>
    <TopNav />
    <div class="px-20 w-full flex flex-wrap">
      <div v-for="arr in subArrays" :key="arr" class="w-1/5">
        <div v-for="card in arr" :key="card" class="w-full">
          <div class="w-full p-2">
            <Card :src="card.src" class="w-full h-full" />
            <div class="">
              <p class="font-bold"></p>
              <p></p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopNav from "./TopNav.vue";
import Card from "./Card.vue";
export default {
  components: {
    TopNav,
    Card,
  },
  computed: {
    subArrays() {
      var length = Math.ceil(this.cards.length / 5);
      const result = new Array(length)
        .fill()
        .map((i) => {
          console.log(i)
          return this.cards.splice(0, length)
        })
        return result
    }
  },
  data() {
    return {
      cards: [
        { src: "1.jpg" },
        { src: "2.jpg" },
        { src: "3.jpg" },
        { src: "4.jpg" },
        { src: "5.jpg" },
        { src: "6.jpg" },
        { src: "7.jpg" },
        { src: "8.jpg" },
        { src: "9.jpg" },
        { src: "10.jpg" },
        { src: "11.jpg" },
        { src: "12.jpg" },
        { src: "13.jpg" },
        { src: "14.jpg" },
        { src: "15.jpg" },
        { src: "16.jpg" },
        { src: "17.jpg" },
        { src: "18.jpg" },
        { src: "19.jpg" },
        { src: "20.jpg" },
        { src: "21.jpg" },
        { src: "22.jpg" },
        { src: "23.jpg" },
        { src: "15.jpg" },
        { src: "5.jpg" },
       
      ],
    };
  },
};
</script>

<style>
</style>
