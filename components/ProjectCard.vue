<template>
  <div ref="singleCard" class="card has-border-radius-4">
    <div class="card-image">
      <figure class="image is-5by4">
        <img
          ref="image"
          class="black-white"
          :src="project.image"
          alt="Project image"
          style="filter: grayscale(100%)"
        />
      </figure>
    </div>
    <div class="card-content" @mouseenter="hoverColors" @mouseleave="normalColors">
      <div class="media">
        <div class="media-left">
          <figure class="image is-48x48 has-border-radius-4">
            <img
              ref="techImage"
              class="black-white"
              style="filter: grayscale(100%)"
              v-bind:class="{ 'invert-color': project.github}"
              :src="project.technologyImage"
              alt="Technology logo"
            />
          </figure>
        </div>
        <div class="media-content has-margin-top-15">
          <p class="title is-6">{{ project.title }}</p>
        </div>
      </div>

      <div class="content is-size-7" v-show="!hover">
        <span>{{ project.description }}</span>
        <br />
        <time datetime="2016-1-1">{{ project.projectDate }}</time>
      </div>

      <div class="content has-text-centered" v-show="hover">
        <a
          v-show="!project.github"
          class="button is-small is-dark is-outlined is-inverted"
          target="_blank"
          rel="noreferrer"
          :href="project.link"
        >
          <span class="icon is-small">
            <i class="fas fa-code"></i>
          </span>
          <span>Source code</span>
        </a>
        <a
          v-show="project.github"
          class="button is-small is-dark is-outlined is-inverted"
          target="_blank"
          rel="noreferrer"
          :href="project.link"
        >
          <span class="icon is-small">
            <i class="fab fa-github"></i>
          </span>
          <span>Github</span>
        </a>
      </div>

      <div class="go-corner" href="#">
        <div class="go-arrow">→</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: false
    };
  },

  props: {
    project: {
      type: Object,
      required: true
    }
  },

  methods: {
    hoverColors: function() {
      const root = this.$refs["singleCard"];
      this._removeGrayScaleStyle();
      this.hover = true;
      root.style.setProperty("--text-color", "white");
      root.style.setProperty("--gray-scale", "0%");
      root.style.setProperty("--invert", "100%");
    },

    normalColors: function() {
      const root = this.$refs["singleCard"];
      this.hover = false;
      root.style.setProperty("--text-color", "black");
      root.style.setProperty("--gray-scale", "100%");
      root.style.setProperty("--invert", "0%");
    },

    _removeGrayScaleStyle: function() {
      // Method used to remove the initial style of the two images of the card, from now on it will be managed my mouse events
      const image = this.$refs["image"];
      const techImage = this.$refs["techImage"];
      image.style = "";
      techImage.style = "";
    }
  }
};
</script>

<style scoped>
:root {
  --text-color: black;
  --gray-scale: 100%;
  --invert: 0%;
}

.black-white {
  transition: all 0.3s ease-out;
  filter: grayscale(var(--gray-scale));
}

.invert-color {
  filter: invert(var(--invert));
}
.has-border-radius-4 {
  border-radius: 4px;
}

.card {
  box-shadow: 0 0 11px rgba(33, 33, 33, 0.2);
}

.go-corner {
  display: flex;
  align-items: center;
  justify-content: center;
  position: absolute;
  width: 32px;
  height: 32px;
  overflow: hidden;
  top: 0;
  right: 0;
  background-color: #363636;
  border-radius: 0 0 0 32px;
}

.go-arrow {
  margin-top: -4px;
  margin-right: -4px;
  color: white;
  font-family: courier, sans;
}

.card-content {
  color: var(--text-color);
  min-height: 220px;
  height: 100%;
  position: relative;
  display: block;
  padding: 32px 24px;
  text-decoration: none;
  z-index: 0;
  overflow: hidden;
}

.card-content:before {
  content: "";
  position: absolute;
  z-index: -1;
  top: -16px;
  right: -16px;
  background: #363636;
  height: 32px;
  width: 32px;
  border-radius: 32px;
  transform: scale(1);
  transform-origin: 50% 50%;
  transition: transform 0.55s ease-out;
}

.card-content:hover::before {
  transform: scale(45);
}

@media screen and (max-width: 1407px) {
  .card-content {
    position: relative;
    min-height: 230px;
  }
}

@media screen and (max-width: 983px) {
  .card-content {
    position: relative;

    min-height: 250px;
  }
}

@media screen and (max-width: 863px) {
  .card-content {
    position: relative;

    min-height: 270px;
  }
}

@media screen and (max-width: 768px) {
  .card-content {
    position: relative;
    min-height: 220px;
  }
}

* {
  transition: all 0.3s ease-out;
}

.title {
  color: var(--text-color) !important;
}
.has-margin-top-15 {
  margin-top: 15px;
}
</style>