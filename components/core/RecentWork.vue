<template>
  <div id="recent-work-section">
    <svg
      class="curveDownColor"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
    >
      <path fill="#fff" d="M0 0 C 50 100 80 100 100 0 Z"></path>
    </svg>
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
        <v-col cols="4" v-for="i in 8" :key="i" class="result-col">
          <div class="cover">
            <img
              width="100%"
              height="100%"
              :src="require(`~/assets/images/work/${i + 1}-big.jpg`)"
              alt=""
              srcset=""
            />
          </div>
        </v-col>
      </v-row>
    </div>
    <div class="view-more mt-8 mb-4">
      <center>
        <v-btn class="more-btn"> VIEW MORE</v-btn>
      </center>
    </div>

    <!-- CurveUp -->
    <svg
      class="curveUpColor bottom-none"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
    >
      <path fill="#fff" d="M0 100 C 20 0 50 0 100 100 Z"></path>
    </svg>
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
#recent-work-section {
  background: #ecf0f1;
  h2 {
    padding-top: 50px;
  }
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
