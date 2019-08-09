<template>
  <section class="hero is-white is-fullheight">
    <div id="banner" class="hero-body" data-aos="fade-right">
      <div class="container" style="z-index: 1;">
        <h2 class="subtitle font-color">Hi,</h2>
        <h1 class="title is-1 font-color">I'm Leonardo</h1>
        <h2 class="subtitle is-2 font-color">Welcome to my page</h2>
        <a class="button is-dark is-outlined is-small font-color">Projects</a>
        <a class="button is-dark is-outlined is-small font-color" v-scroll-to="{el: '#footer', duration: 1500}">Get in touch</a>
      </div>
    </div>
    <!-- dont ask how -->
    <div class="header-bg " data-aos="fade-left">
        <div style="width: 100%; padding-bottom: 66.6667%;"></div>
        <picture>
            <img src="./../static/surface.jpg" />
        </picture>
    </div>
  </section>
</template>

<style>
.header-bg {
    overflow: hidden;
    position: absolute;
    width: 50vw;
    height: 100vh;
    background-size: cover;
    background-position: 50%;
    right: 0;
    
}
@media only screen and (max-width: 80rem) {
  .header-bg {
    width: 100vw;
  }
  .font-color {
    color:white !important;
  }
}


img {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center center;
    opacity: 1;
    transition: opacity 0.5s ease 0s;
}
</style>

<script>
export default {};
</script>
