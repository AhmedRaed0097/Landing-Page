<template>
  <div class="footer-container">
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
    <div class="footer-wrapper">
      <v-container>
        <v-row>
          <v-col cols="3">
            <div class="about">
              <h3>About</h3>
              <p>
                Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed
                diam nonumy eirmod tempor invidunt ut labore.
              </p>
              <p>Et dolore magna aliquyam erat sed diam voluptua.</p>
            </div>
          </v-col>
          <v-col cols="3">
            <div class="recent-postes">
              <h3>RecentPostes</h3>
              <ul>
                <li>Suspendisse nec lectus non</li>
                <li>Phasellus euismod pulvinar</li>
                <li>Aliquam erat volutpat</li>
                <li>Phasellus euismod pulvinar</li>
                <li>Aliquam erat volutpat</li>
              </ul>
            </div>
          </v-col>
          <v-col cols="3">
            <div class="more-info">
              <h3>More Info</h3>
              <p>
                Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed
                diam nonumy eirmod tempor invidunt ut labore.
              </p>
              <p>Et dolore magna aliquyam erat sed diam voluptua.</p>
            </div>
          </v-col>
          <v-col cols="3">
            <div class="more-info">
              <h3>Flickr Feed</h3>
              <div class="images-container">
                <v-row>
                  <v-col cols="4" v-for="i in 5" :key="i">
                    <img
                      class="flicker-images"
                      width="75"
                      :src="
                        require(`~/assets/images/flickr-widget/flickr${
                          i + 1
                        }.jpg`)
                      "
                      alt="flickr image"
                    />
                  </v-col>
                </v-row>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
      <center>
        <p style="position: relative; top: 55px">
          © 2022 | All Rights Reserved Created By
          <span style="color: #1abc9c">Ahmed Raed</span>
        </p>
      </center>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer-container {
  width: 100%;
  color: #fff;
  background: #2c2d31;
  height: 600px;
  .footer-wrapper {
    margin-top: 60px;
    h3 {
      font-size: 1.8rem;
      margin-bottom: 30px;
    }
    ul {
      line-height: 3;
      list-style: none;
      li:before {
        content: "\2022"; /* Add content: \2022 is the CSS Code/unicode for a bullet */
        color: #1abc9c;
        width: 1.2em;
        font-weight: bold;
        display: inline-block;
      }
    }
    p {
      line-height: 2;
    }
  }
}
.images-container {
  .row {
    width: 300px;
    .col-4 {
      flex: 0 0 33.3333333333%;
      max-width: 27.333333%;
    }
    .col {
      padding: 0;
      .flicker-images {
        border-radius: 7px;
        float: right;
        margin-bottom: 7px;
      }
    }
  }
}
</style>
