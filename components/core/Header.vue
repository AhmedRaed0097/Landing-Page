<template>
  <section class="header-container">
    <section class="header-text">
      <h2>WE ARE CREATIVE DESIGN AGENCY</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Illum, fuga,
        consectetur sequi consequuntur nisi placeat ullam maiores perferendis.
        Quod, nihil reiciendis saepe optio libero minus et beatae ipsam
        reprehenderit sequi.
      </p>
      <div>
        <v-btn rounded outlined color="#fff">Find Out More</v-btn>
      </div>
    </section>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header-container {
  width: 100vw;
  height: 700px;
  padding: 20px;
  position: absolute;
  top: -64px;
  left: 0;
  background-image: url("@/assets/images/home.jpg");
  // clip-path: polygon(100% 0%, 73% 0%, 0% 0%, 0% 0%, 0% 25%, 0% 38%, 0% 63%, 17% 54%, 32% 50%, 53% 49%, 80% 52%, 89% 57%, 100% 67%, 100% 25%);
}
.header-text {
  height: 300px !important;
  width: 50%;
  color: #fff;
  position: absolute;
  right: 0;
  bottom:50px;
  transform: translate(-50%, -50%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  h2 {
    font-size: 2.5em;
  }
  p {
    margin-top: 50px;
    margin-bottom: 40px;
    width: 770px;
    text-align: center;
  }
  .v-btn{
    padding: 22px 20px;
    border: 2px solid #fff;
  }
}
</style>
