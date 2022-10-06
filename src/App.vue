<template>
  <div id="nav">
    <div class="links">
      <router-link class="link" to="/" @click="toWhite">Ergonomics</router-link> |
      <router-link class="link" to="/voice" @click="toBlack">Voice Control</router-link>
    </div>
  </div>
  <router-view />
</template>

<script>
export default {
  methods: {
    toBlack: function () {
      let app = document.getElementById('app');
      app.classList.add("back-black")
    },

    toWhite: function () {
      let app = document.getElementById('app');
      app.classList.remove("back-black")
    }
  }
}
</script>
