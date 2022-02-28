<template>
  <div class="our-blog-container" id="our-blog-section">
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
    <h2 class="our-blog-title section-title mt-16 mb-16">OUR BLOG</h2>
    <section class="result-container">
      <v-row>
        <v-col md="6" v-for="i in 4" :key="i" class="blog-result-col">
          <v-card>
            <div class="blog-container">
              <div class="blog-cover">
                <img
                  width="100%"
                  src="~/assets/images/post/post-n2.jpg"
                  alt="post-cover"
                />
              </div>
              <div class="blog-title">
                <p>Lorem ipsum dolor sit.</p>
              </div>

              <div class="blog-date">
                <small>26 March, 2014 · Graphic Design</small>
              </div>

              <div class="blog-description">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nulla,
                sequi, quas, assumenda harum nam reiciendis obcaecati maxime
                suscipit quibusdam.
              </div>
              <div class="button-container">
                <v-btn class="more-btn">Reas More</v-btn>
              </div>
            </div>
          </v-card>
        </v-col>
      </v-row>
      <div class="view-more mt-8 mb-4">
        <center>
          <v-btn class="more-btn"> VIEW MORE</v-btn>
        </center>
      </div>
    </section>
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
export default {};
</script>

<style lang="scss" scoped>
.our-blog-container {
  background: #ecf0f1;
}
.blog-result-col {
  .v-card {
    padding-bottom: 30px;
    border-radius: 9px 9px 0 0;
    margin-bottom: 10px;
    img {
      border-radius: 7px 7px 0 0;
    }
    .blog-container {
      display: flex !important;
      flex-direction: column !important;
      justify-content: center !important;
      align-items: center !important;
      gap: 20px;
      .blog-title {
        color: #1abc9c;
        font-size: 1.5rem;
      }
      .blog-date {
        color: #1abc9c;
        font-size: 0.8rem;
        margin-top: -15px;
        margin-bottom: 15px;
      }
      .blog-description {
        text-align: center;
        padding: 0 60px !important;
      }
    }
  }
}
</style>
