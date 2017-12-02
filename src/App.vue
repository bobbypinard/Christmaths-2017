<template>
  <div id="app">
    <h1>Add some layers to the Fibonacci tree.</h1>
    <div class="form-group">
      <b-button @click="addLayer" variant="default" name="button">Add layer</b-button>
      <b-button @click="layer = 0" variant="default" name="button">Reset</b-button>
    </div>

    {{ layer }}  <!-- Testing -->
    <div class="star">
      <h1>Ho</h1>
    </div>
    <div class="tree">
      {{ text }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      layer: 0
    }
  },
  methods: {
    addLayer: function() {
      return this.layer += 1
    }
  },
  computed: {
    text: function() {
      if (this.layer >= 2) {
        return "Ho Ho"
      } else if (this.layer >= 1) {
        return "Ho"
      } else if (this.layer >= 0) {
        return "Ho"
      } else {
        return "Error"
      }
    }
  }
}
</script>

<style lang="scss">
body {
  background-color: red;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #FFF;
  margin-top: 60px;
}

.tree {
  font-size: 1.5em;
  color: #7FFF00;
}
</style>
