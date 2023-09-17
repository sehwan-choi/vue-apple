<template>
  <div>
    <app-header 
      v-bind:propsdata="str" 
      v-on:renew="renewString"></app-header>
      <app-header 
        v-bind:propsdata="str2" 
        v-on:keyOn="keyString"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'

export default {
  name: 'App',
  data: function() {
    return {
      str: 'Header',
      str2: 'No Text'
    }
  },
  components: {
    'app-header': AppHeader
  }, 
  methods: {
    renewString: function(val) {
      this.str = val;
    },
    keyString: function(val) {
      this.str2 = val;
    }
  }
}
</script>

<style>

</style>