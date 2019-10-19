<template>
  <div>
    <Navbar />

    <Banner />

    <Timeline />

    <Skills />

    <Footer />
  </div>
</template>

<script>
import Navbar from "~/components/Navbar.vue";
import Timeline from "~/components/Timeline.vue";
import Banner from "~/components/Banner.vue";
import Skills from "~/components/Skills.vue";
import Footer from "~/components/Footer.vue";
import AOS from "aos";
import "aos/dist/aos.css";

AOS.init();

export default {
  components: {
    Timeline,
    Banner,
    Skills,
    Footer,
    Navbar
  },

  head() {
    return {
      title: "Leo's page"
    };
  }
};
</script>

<style>
.links {
  padding-top: 15px;
}

.has-text-centered {
  text-align: center;
}

.columns.is-vcentered {
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}

.small-border-radius {
  border-radius: 3px;
}

.has-margin-right {
  margin-right: 0.5em;
}
</style>
