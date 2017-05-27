<template>
  <div>
    <label class="typo__label">Simple select / dropdown</label>
    <multiselect
    v-model="value" :options="optionsArray" :multiple="true" :close-on-select="false"
    :clear-on-select="false" :hide-selected="true" placeholder="Pick some" label="name" track-by="name"/>
    <!-- <pre class="language-json"><code>{{ value }}</code></pre> -->
  </div>
</template>

<script>
import Multiselect from '~assets/vendor/vue-multiselect/Multiselect'

export default {
  components: {
    Multiselect
  },
  props: {
    optionsArray: Array
  },
  data () {
    return {
      value: []
    }
  }
}
</script>
