<template>
  <section class="hero is-light is-fullheight">
    <div class="hero-body">
      <div class="container" style="z-index: 1;">
        <div class="columns is-vcentered is-variable is-8">
          <div
            class="column is-one-third"
            v-for="index in projectToDisplay"
            data-aos="fade-up"
            :data-aos-delay="index * 100"
            :key="index"
          >
            <ProjectCard :project="projects[index - 1]" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<script>
import ProjectCard from "~/components/ProjectCard.vue";

export default {
  components: {
    ProjectCard
  },
  data: function() {
    return {
      projectToDisplay: 3,
      projects: [
        {
          image: "mockup-django.jpg",
          title: "Django forum",
          description:
            "Made with Django2 (python web framework) and Bootstrap4, this project is a forum with classic functionalities.",
          technologyImage: "python.jpg",
          projectDate: "Jan 2019",
          link: "https://github.com/leobia/django-forum"
        },
        {
          image: "movie-search.jpg",
          title: "Movie finder",
          description:
            "A simple movie finder built with nuxtjs (Vue). The movies are provided by OMDB apis",
          technologyImage: "vue.jpg",
          projectDate: "Sep 2019",
          link: "https://github.com/leobia/movie-search"
        },
        {
          image: "mockup-django.jpg",
          title: "More coming soon..",
          description: "You can find all my projects on github...",
          technologyImage: "github.jpg",
          projectDate: "",
          link: "https://github.com/leobia",
          github: true
        }
      ]
    };
  }
};
</script>

<style>
</style>