<script>

export default {
  components: {
    name: "AppNavbar",
  },
  data() {
    return {
      UtilitiesLogos: [
        {image: "buy-comics-digital-comics.png", paragr:"DIGITAL COMICS"},
        {image: "buy-comics-merchandise.png", paragr:"DC MERCHANDISE"},
        {image:"buy-comics-subscriptions.png", paragr:"SUBSCRIPTION"},
        {image:"buy-dc-power-visa.svg", paragr:"DC POWER VISA"},
      ]
    }
  },
  methods: { 
    getImagePathBy
  },
}
</script>

<template>
  <div class="ms_container">
    <div v-for="(item, index) in UtilitiesLogos">
      <img :src="`../assets/${UtilitiesLogos.image}`" alt="">
      <p>{{ UtilitiesLogos.paragr }}</p>
    </div>
  </div>
    
</template>

<style lang="scss" scoped>
  .ms_container {
  width: 100%;
  margin: 0 auto;
  padding: 3% 10%;
  background-color: #157cea;
  color: white;
}

</style>