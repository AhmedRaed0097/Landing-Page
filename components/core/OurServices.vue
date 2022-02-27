<template>
  <div class="our-services-container" id="our-service-section">
      <h2 class="our-service-title section-title">OUR SERVICES</h2>
    <v-row>
      <v-col lg="3" v-for="i in 4" :key="i">
        <section class="service-container">
          <div class="icon">
            <p>ICON</p>
          </div>
          <h3 class="service-title">Lorem, ipsum dolor.</h3>
          <p class="description">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit.
            Perspiciatis voluptatem corporis nobis ea dolorum veniam natus hic.
            Ratione .
          </p>
          <v-btn class="more-btn"
            >Read More</v-btn
          >
        </section>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      services: [{}],
    };
  },
};
</script>
