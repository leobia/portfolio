<template>
  <div>
    <nav class="navbar is-transparent is-fixed-top" role="navigation" aria-label="main navigation">
      <div class="navbar-item">Leo's page</div>
    </nav>

    <Banner />

    <Timeline />

    <section class="hero is-white is-fullheight">
      <div class="hero-body">
        <div class="container" style="z-index: 1;">
          <div class="columns is-vcentered">
            <div class="column is-half has-text-centered">
              <h2 class="subtitle is-2">Skills</h2>
              <div>
                From the time I started my journey as a web developer, I have been constantly learning new things. In fact I'm always trying to expand my skillset by reading articles, watching videos and experimenting new technologies.
              </div>
            </div>
            <div class="column is-half">
              <div class="box small-border-radius">
                <h3 class="title is-6 has-text-centered">Back-end</h3>
                <hr>
                <h3 class="title is-6 has-text-centered">Front-end</h3>
                <hr>
                <h3 class="title is-6 has-text-centered">Development Tools</h3>
              </div>
              <!-- <div class="box no-border-radius">
                <h3 class="title is-6 has-text-centered">Front-end</h3>
              </div>
              <div class="box no-border-radius">
                <h3 class="title is-6 has-text-centered">Development Tools</h3>
              </div> -->
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Timeline from "~/components/Timeline.vue";
import Banner from "~/components/Banner.vue";

export default {
  components: {
    Timeline,
    Banner
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
