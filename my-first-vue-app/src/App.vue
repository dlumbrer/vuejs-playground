<template>
  <div id="app">
    <div class="navbar has-shadow">
      <div class="container">
        <div class="navbar-start">
          <a class="navbar-item">Raistlin</a>
        </div>

        <span class="navbar-burger" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
          <span></span>
          <span></span>
          <span></span>
        </span>

        <div class="navbar-end navbar-menu" v-bind:class="{ 'is-active': isActive }">
          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="/faq" class="navbar-item r-item">FAQ</router-link>

          <div class="navbar-item">
            <p class="control">
              <a class="button is-primary is-outlined">
                <span class="icon">
                  <i class="fa fa-download"></i>
                </span>
                <span>Join Now</span>
              </a>
            </p>
          </div>

        </div>

      </div>
    </div>
    <router-view/>
    
    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>Example of some text in the footer!</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fa fa-play"></i></a>
            <a class="icon" href="#"><i class="fa fa-stop"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function () {
      this.isActive = !this.isActive
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'

.navbar
  background-color: #383838
  a:hover
    color: gray

.navbar-start a
  color: white
  font-weight: bold

a.r-item
  color: #C1C1C1
  padding: 0.5rem 1.75rem

.navbar-burger span
  background-color: #C1C1C1

footer
  background-color: $primary !important
  color: white
</style>
