<template>
  <section class="hero is-white is-fullheight">
    <div id="banner" class="hero-body" data-aos="fade-right">
      <div class="container" style="z-index: 1;">
        <h2 class="subtitle">Hi,</h2>
        <h1 class="title is-1">I'm Leonardo</h1>
        <h2 class="subtitle is-2">Welcome to my page</h2>
        <button class="button is-dark is-outlined is-small is-rounded">Projects</button>
        <button class="button is-dark is-outlined is-small is-rounded">About</button>
      </div>
    </div>
    <!-- dont ask how -->
    <div class="header-bg " data-aos="fade-left">
        <div style="width: 100%; padding-bottom: 66.6667%;"></div>
        <picture>
            <img src="./../static/header.jpg" />
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
}

.header-bg @media (max-width: 80rem) {
    width: 100vw;
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
