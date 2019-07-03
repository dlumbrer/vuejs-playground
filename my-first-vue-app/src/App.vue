<template>
  <div id="app">
    <div class="navbar has-shadow">
      <div class="container">
        <div class="navbar-start">
          <a class="navbar-item">Raistlin</a>
        </div>

        <span class="navbar-toggle">
          <span></span>
          <span></span>
          <span></span>
        </span>

        <div class="navbar-end navbar-menu">
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
  </div>
</template>

<script>
export default {
  name: 'App'
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
</style>
