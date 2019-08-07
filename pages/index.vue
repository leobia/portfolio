<template>
  <div>
    <nav class="navbar is-transparent is-fixed-top" role="navigation" aria-label="main navigation">
      <div class="navbar-item">Leo's page</div>
    </nav>

    <Banner />

    <Timeline />

    <Skills />

  </div>
</template>

<script>
import Timeline from "~/components/Timeline.vue";
import Banner from "~/components/Banner.vue";
import Skills from "~/components/Skills.vue";

export default {
  components: {
    Timeline,
    Banner,
    Skills
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
</style>
