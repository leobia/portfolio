<template>
  <section class="hero is-white is-fullheight">
    <div class="hero-body">
      <div class="container" style="z-index: 1;">
        <div class="columns is-vcentered">
          <div class="column is-half has-text-centered" data-aos="fade-right">
            <h2 class="subtitle is-2">Skills</h2>
            <div>From the time I started my journey as a web developer, I have been constantly learning new things. In fact I'm always trying to expand my skillset by reading articles, watching videos and experimenting new technologies.</div>
          </div>
          <div class="column is-half" data-aos="fade-left">
            <div class="box small-border-radius">
              <h3 class="title is-6 has-text-centered">Back-end</h3>
              <div class="tags">
                <span class="tag is-dark" v-for="(skill, index) in backEndSkills" :key="index">{{skill}}</span>
              </div>
              <hr />
              <h3 class="title is-6 has-text-centered">Front-end</h3>
              <div class="tags">
                <span class="tag is-dark" v-for="(skill, index) in frontEndSkills" :key="index">{{skill}}</span>
              </div>
              <hr />
              <h3 class="title is-6 has-text-centered">Development Tools</h3>
              <div class="tags">
                <span class="tag is-dark" v-for="(skill, index) in devTools" :key="index">{{skill}}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
    .tag {
        width: 6em;
    }
    .tags {
        justify-content: center;
    }
</style>

<script>
export default {
  data: function() {
    return {
      backEndSkills: ["Java", "Spring", "JEE", "JSF", "Python", "Django"],
      frontEndSkills: ["ES6", "HTML", "CSS", "Vue", "jsp"],
      devTools: ["IntelliJ", "VS Code", "Eclipse", "Netbeans"]
    };
  }
};
</script>
