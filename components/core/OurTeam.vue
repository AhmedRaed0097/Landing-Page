<template>
  <div
    class="our-team-container"
    id="our-team-section"
    style="margin-bottom: 300px !important; margin-top: 300px !important"
  >
    <svg
      class="curveDownColor top-none"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="100"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
    >
      <path fill="#fff" d="M0 0 C 50 100 80 100 100 0 Z"></path>
    </svg>
    <div class="team-content">
      <h2 class="our-team section-title">OUR TEAM</h2>
      <section>
        <v-row>
          <v-col md="3" v-for="(member, index) in teamMembers" :key="index">
            <v-card class="member-card">
              <div class="img-container">
                <img
                  width="100%"
                  :src="require(`~/assets/images/team/user${index + 1}.png`)"
                  alt="team member"
                />
              </div>

              <div class="accounts">
                <v-icon>mdi mdi-facebook</v-icon>
                <v-icon>mdi mdi-twitter</v-icon>
                <v-icon>mdi mdi-google-plus</v-icon>
                <v-icon>mdi mdi-linkedin</v-icon>
              </div>
              <div class="member-data">
                <p class="name">{{ member.name }}</p>
                <p class="rank">{{ member.rank }}</p>
              </div>
            </v-card>
          </v-col>
        </v-row>
      </section>
      <svg
        class="curveUpColor"
        style="position: absolute; bottom: 0; left: 4px"
        xmlns="http://www.w3.org/2000/svg"
        version="1.1"
        width="100%"
        height="100"
        viewBox="0 0 100 100"
        preserveAspectRatio="none"
      >
        <path fill="white" d="M0 100 C 20 0 50 0 100 100 Z"></path>
      </svg>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      teamMembers: [
        {
          name: "Tim Malkovic",
          rank: "CEO",
        },
        {
          name: "David Bell",
          rank: "Creative Designer",
        },
        {
          name: "Eva Stinger",
          rank: "Sales Manager",
        },
        {
          name: "Will Peters",
          rank: "Developer",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.our-team-container {
  margin-bottom: 300px !important;
  margin-top: 300px !important;
  height: 1300px !important;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #ecf0f1;

  .section-title {
    margin-bottom: 50px !important;
  }
}
.member-card {
  border-radius: 8px;
  &:hover {
    .accounts {
      // bottom: 70px;
      height: 45px;
      // z-index: 1;
      opacity: 1;
    }
  }
  img {
    border-radius: 8px 8px 0 0;
  }
  .member-data {
    background: #fff;
    height: 70px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    padding-bottom: 12px;
    .name {
      font-size: 1.3rem;
    }
    .rank {
      font-size: 0.9rem;
      color: #1abc9c;
    }
  }
}
.accounts {
  // z-index: -1;
  opacity: 0;
  background: #fff;
  height: 45px;
  position: absolute;
  bottom: 70px;
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  transition: all 0.3s ease;
}
.team-content {
  width: 70%;
}
</style>
