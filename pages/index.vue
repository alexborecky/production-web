<template>
  <div class="main-container">
    <div class="full flex column center">
      <div class="container flex column">
        <h1>Hi, I’m Alex! An award winning director, actor, screenwriter and producer.</h1>
        <div class="projects">
          <nuxt-link to="/untold" class="featured project">
            <div class="project-info">
              <h2>Untold Pieces</h2>
              <p>2023</p>
            </div>
            <div class="blur-layer"></div>
          </nuxt-link>
          <div class="project-row flex">
            <nuxt-link to="/origin" class="project">
              <div class="project-info">
                <h2>Origin</h2>
                <p>2021</p>
              </div>
              <div class="blur-layer"></div>
            </nuxt-link>
            <nuxt-link to="/precedenti" class="project">
              <div class="project-info">
                <h2>Precedenti</h2>
                <p>Pre-production</p>
              </div>
              <div class="blur-layer"></div>
            </nuxt-link>
          </div>
        </div>
        <pageFooter />
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="scss">

.hero {
  background-size: cover;
  min-height: 100vh;
  @media (max-width: 500px) {
    background-position: center;
  }
}
.container {
  text-align: center;
  h1 {
    margin-top: 160px;
  }
  .projects {
    margin: 80px 0;
    .featured {
      width: 100%;
      height: 480px;
      background-image: url(https://ik.imagekit.io/alexborecky/FILM_WEB/UP_Awards_qfPEteTeF.jpg?updatedAt=1686554969927);
      background-position: center;
      background-size: cover;
      background-repeat: no-repeat;
      @media (max-width: 1280px) {
        height: 360px;
      }
    }
    .project-row {
      margin-top: 40px;
      height: 360px;
      justify-content: space-between;
      width: 100%;
      .project {
        width: calc(50% - 20px);
        height: 100%;
        background-size: cover;
        &:first-child {
          background-image: url(https://ik.imagekit.io/alexborecky/FILM_WEB/Origin_Awards_ksYiUqJfY.jpg?updatedAt=1686496129090);
        }
        &:nth-child(2) {
          background-image: url(https://ik.imagekit.io/alexborecky/FILM_WEB/Frame_26_RG9awGofA.jpg?updatedAt=1686496414029);
        }
      }
      @media (max-width: 1280px) {
        height: 240px;
      }
    }
  }
}
</style>
