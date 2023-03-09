<script lang="ts">
import HeaderNav from "../components/main/header-nav.vue";
import { defineComponent, computed } from "vue";

export default defineComponent({
  components: {
    HeaderNav,
  },
  props: {
    loggedIn: Boolean,
  },
  data() {
    return {
      loggedIn: false,
    }
  },
  computed: {
    isLoggedIn(): Boolean {
      return this.loggedIn;
    }
  }
})
</script>

<template>
  <HeaderNav />
  <div class="hero">
    <div class="hero-container">
      <div class="app-description-container">
        <h2 class="app-description">
          Generate your Spotify music <br />
          <em>festival playlist</em><br />
          and hype up your next music event
        </h2>
        <a href="/"><button class="hero-button"> Get Started</button></a>
      </div>
      <div class="hero-image-container">
        <img
          alt="Vue logo"
          class="hero-image"
          src="@/assets/music_hero.svg"
          height="600px"
        />
      </div>
    </div>
    <div class="landing-content"></div>
  </div>
</template>

<style scoped>
.hero {
  background-color: var(--color-main);
  display: flex;
  color: white;
  padding: 5rem;
  justify-content: center;
}

.hero-container {
  display: flex;
  justify-content: space-between;
  width: 85%;
  font-size: 1.15rem;
}

em {
  font-size: 3.75rem;
  font-style: normal;
  font-weight: 800;
}

.app-description {
  line-height: 3rem;
}

.hero-image-container {
  position: relative;
}

.hero-image {
  position: absolute;
  top: -150px;
  right: -150px;
}

.hero-button {
  margin-top: 3rem;
  background-color: rgb(20, 20, 20);
  outline: none;
  color: white;
  font-family: "Inter";
  font-size: 1.25rem;
  font-weight: 800;
  padding: 0.75rem 0;
  border: none;
  border-radius: 99px;
  cursor: pointer;
  width: 100%;
}
</style>
