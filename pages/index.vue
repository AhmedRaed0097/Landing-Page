<template>
  <div>
    <!--  -->
    <Header  />
    <OurServices class="component"/>
    <RecentWork class="component" />
    <Carousel class="component" :objectType="'qoutes'" />
    <OurBlog class="component" />
    <PricingTables class="component small-component" />
    <OurTeam  class="component small-component" />
    <Carousel class="component" :objectType="'brands'" />
    <ContacUs class="component" />
  </div>
</template>

<script>
import PricingTables from "@/components/core/PricingTables";
import OurServices from "@/components/core/OurServices";
import ContacUs from "@/components/core/ContacUs.vue";
import RecentWork from "@/components/core/RecentWork";
import Carousel from "@/components/core/Carousel";
import OurTeam from "@/components/core/OurTeam";
import OurBlog from "@/components/core/OurBlog";
import Header from "@/components/core/Header";
export default {
  components: {
    PricingTables,
    OurServices,
    RecentWork,
    OurTeam,
    Carousel,
    ContacUs,
    OurTeam,
    OurBlog,
    Header,
  },
};
</script>

<style lang="scss" scoped>
.component {
  margin: 100px  auto !important;
  position: relative;
}
</style>
