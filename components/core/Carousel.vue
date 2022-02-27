<template>
  <div class="carousel-container">
    <client-only>
      <!-- important to add no-ssr-->

      <carousel
        class="qoutes-carousel"
        v-if="objectType === 'qoutes'"
        :items="1"
        :nav="false"
        :center="true"
      >
        <div v-for="i in 4" :key="i" class="carousel-item-container">
          <img
            class="icon-carousel"
            width="50"
            height="40"
            src="~/assets/images/quotes.svg"
            alt="quotes"
          />
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. In unde
            odio nobis eaque aliquid, totam, repellendus blanditiis fugit.
          </p>
          <h3>Lorem ipsum.</h3>
        </div>
      </carousel>

      <carousel
        class="brands-carousel"
        v-if="objectType === 'brands'"
        :items="6"
        :nav="false"
        :center="true"
        :loop="true"
        :dotsData="true"
        :dots="true"
        :autoplay="true"
        :autoplayTimeout="3000"
        :autoplaySpeed="1000"
        :margin="20"
        :stagePadding="100"
      >
        <div v-for="i in 4" :key="i" class="carousel-item-container">
          <img
            width="30"
            :src="require(`~/assets/images/clients/${i + 1}.png`)"
            alt="brand"
          />
        </div>
      </carousel>
    </client-only>
  </div>
</template>

<script>
export default {
  props: {
    objectType: {
      type: String,
      default: "",
    },
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.carousel-container {
  margin-top: 150px;
   width: 65vw;
  .carousel-item-container {
    display: flex;
    flex-direction: column;
    gap: 20px;
    text-align: center;
  }
}
.icon-carousel {
  transform: rotate(180deg);
}


</style>
