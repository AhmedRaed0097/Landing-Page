<template>
  <div class="footer-container">
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
                    width="100%"
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
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer-container{
  height: 600px;
}
</style>
