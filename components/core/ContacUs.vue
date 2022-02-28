<template>
  <div class="contact" id="contanct-section" style="margin-top: 350px !important;margin-bottom: 550px !important; ">
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
    <div style="width: 60vw;margin: 0 auto;height: 1030px;">
      <h2 class="contact-title section-title mb-16">CONTACT</h2>
      <v-row>
        <v-col cols="6">
          <v-row>
            <v-col cols="12">
              <h3 class="adress-section-title">Talks to us</h3>
            </v-col>
            <v-col cols="12">
              <p>
                Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                Dolores iusto fugit esse soluta quae debitis quibusdam harum
                voluptatem, maxime, aliquam sequi. Tempora ipsum magni unde
                velit corporis fuga, necessitatibus blanditiis.
              </p>
            </v-col>
            <v-col cols="12">
              <div class="wrapper">
                <div class="address address-item">
                  <div class="icon">
                    <img src="~/assets/svg/location.svg" alt="location-icon" />
                  </div>
                  <div class="address-body body">
                    <p class="item-title">Address</p>
                    <p class="item-description">
                      9983 City name, Street name, 232 Apartment C
                    </p>
                  </div>
                </div>
                <div class="work-time address-item">
                  <div class="icon">
                    <img src="~/assets/svg/clokc.svg" alt="clock-icon" />
                  </div>
                  <div class="work-time-body body">
                    <p class="item-title">Work Time</p>
                    <p class="item-description">
                      Monday - Friday from 9am to 5pm
                    </p>
                  </div>
                </div>
                <div class="phone address-item">
                  <div class="icon">
                    <img src="~/assets/svg/phone.svg" alt="phone-icon" />
                  </div>
                  <div class="phone-body body">
                    <p class="item-title">Phone</p>
                    <p class="item-description">595 12 34 567</p>
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-col>

        <v-col cols="6">
          <v-form ref="form" v-model="valid" lazy-validation>
            <v-row>
              <v-col cols="12">
                <v-text-field
                  outlined
                  required
                  class="input-field-container contact-field"
                  placeholder="Name"
                  type="text"
                  color="#1abc9c"
                />
              </v-col>
              <v-col cols="12">
                <v-text-field
                  outlined
                  required
                  class="input-field-container contact-field"
                  placeholder="Email"
                  type="text"
                  color="#1abc9c"
                />
              </v-col>
              <v-col cols="12">
                <v-text-field
                  outlined
                  required
                  class="input-field-container contact-field"
                  placeholder="Subject"
                  type="text"
                  color="#1abc9c"
                />
              </v-col>
              <v-col cols="12">
                <v-textarea
                  outlined
                  name="input-7-4"
                  placeholder="Message..."
                  color="#1abc9c"
                ></v-textarea>
              </v-col>
            </v-row>
            <div class="btn-container">
              <v-btn class="more-btn">Send Message</v-btn>
            </div>
          </v-form>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      valid: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.contact {
  background: #ecf0f1;

  *:not(h2) {
    color: #666666;
  }
  .icon {
    height: 56px;
    padding-right: 15px;
    border-right: 2px solid #b9b8b8;
    img {
      width: 25px;
      margin-top: 15px;
    }
  }

  .adress-section-title {
    font-size: 2.2rem;
  }

  .wrapper {
    display: flex;
    flex-direction: column;
    gap: 40px;
    margin-top: 50px;
    .address-item {
      display: flex;
      gap: 18px;
      align-items: center;
    }
  }

  .btn-container {
    .more-btn {
      float: right;
      width: 169px;
    }
  }

  .v-form {
    width: 500px !important;
    float: right !important;
  }

  .contact-title{
    padding-top: 150px !important;
  }
}
</style>
