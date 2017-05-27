<template>
  <section class="container">
    <div>
      <logo/>
      <h1 class="title">
        NUXT
      </h1>
      <h2 class="subtitle">
        Universal Vue.js Application
      </h2>
      <v-select :options-array="fworks"></v-select>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">Documentation</a>
        <a href="https://github.com/nuxt/nuxt.js" target="_blank" class="button--grey">GitHub</a>
      </div>
      <br>
      <h1 class="subtitle">+7 (982) 536-50-77</h1>
    </div>
  </section>
</template>

<script>
import Logo from '~components/Logo.vue'
import VSelect from '~components/Select.vue'

let timeout = (ms) => {
  return new Promise(resolve => setTimeout(resolve, ms))
}

export default {
  components: {
    Logo, VSelect
  },
  data () {
    return {
      fworks: []
    }
  },
  async mounted () {
    let fworks = [
      { name: 'Vue.js', language: 'JavaScript' },
      { name: 'Adonis', language: 'JavaScript' },
      { name: 'Rails', language: 'Ruby' },
      { name: 'Sinatra', language: 'Ruby' },
      { name: 'Laravel', language: 'PHP' },
      { name: 'Phoenix', language: 'Elixir' }
    ]
    await timeout(3000)
    // return {
    this.fworks = fworks
    // }
  }
}
</script>

<style>
.container
{
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.title
{
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
.subtitle
{
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}
.links
{
  padding-top: 15px;
}
</style>
