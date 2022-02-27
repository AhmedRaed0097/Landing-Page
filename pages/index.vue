<template>
  <div style="height: 8000px">
    <!--  -->
    <Header class="component" />
    <OurServices class="component" />
    <RecentWork class="component" />
    <Carousel class="component" :objectType="'qoutes'" />
    <OurBlog class="component" />
    <PricingTables class="component" />
    <OurTeam />
    <Carousel class="component" :objectType="'brands'" />
  </div>
</template>

<script>
import PricingTables from "@/components/core/PricingTables";
import OurServices from "@/components/core/OurServices";
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
    OurTeam,
    OurBlog,
    Header,
  },
};
</script>

<style lang="scss" scoped>
.component {
  margin: 240px  0 !important;
}
</style>
