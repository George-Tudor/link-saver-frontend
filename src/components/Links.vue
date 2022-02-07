<template>
  <div class="hello">
    <h3>{{ title }}</h3>
    <div class="form">
      <div class="form-group">
        <label>Link Address</label>
        <input class="form-control" type="text" v-model="link.address">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Links',
  data() {
    return {
      title: 'Links',
      link: {
        address: '',

      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  font-size: 1.75rem;
  margin: 40px 0 0;
  font-weight: 500;
  line-height: 1.2;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
