<template>
  <div>
    <h2 class="recent-wrok-title section-title">RECENT WORK</h2>

    <div class="filters">
      <span class="filter-item" :class="{ active: selectedType === 'all' }"
        >All</span
      >
      <span
        class="filter-item"
        :class="{ active: selectedType === 'illustration' }"
        >Illustration</span
      >
      <span class="filter-item" :class="{ active: selectedType === 'web' }"
        >Web Design</span
      >
      <span
        class="filter-item"
        :class="{ active: selectedType === 'photography' }"
        >Photography</span
      >
    </div>
    <div class="result-container">
      <v-row>
        <v-col cols="4" v-for="i in 5" :key="i" class="result-col">
          <div class="cover">
            <img
              width="100%"
              height="100%"
              src="~/assets/images/work/5-big.jpg"
              alt=""
              srcset=""
            />
          </div>
        </v-col>
      </v-row>
    </div>
    <div class="view-more mt-8 mb-4">
          <center>

          <v-btn class="more-btn">
        VIEW MORE</v-btn>
          </center>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedType: "all",
    };
  },
  methods: {
    fillterd(type) {
      this.selectedType = type;
    },
  },
};
</script>

<style lang="scss" scoped>
.result-container {
  width: 80vw;
  margin: 0 auto;
}
.result-col {
  padding-top: 0;
  padding-left: 0;
  padding-right: 20px;
  padding-bottom: 15px;
}
.cover {
  width: 100%;
  height: 100%;
  img {
    border-radius: 15px;
  }
}
.filters {
  display: flex;
  justify-content: center;
  // align-items: center;
  gap: 70px;
  margin: 60px 0 50px 0;
  .filter-item {
    text-align: center;
    cursor: pointer;
    min-width: 70px;
      padding: 3px 10px;
    transition: all 0.2s ease;
      border-radius: 30px;
    &:hover {
      border: 2px solid #1abc9c;
      color: #1abc9c;
    }
  }
}
.active {
  border: 2px solid #1abc9c;
  color: #1abc9c;
  border-radius: 30px;
}
</style>
