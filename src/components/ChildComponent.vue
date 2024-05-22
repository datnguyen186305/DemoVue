<!-- HTML -->
<template>
  <div>
    <p>Hello {{yourName}} !</p>
    <button @click="guiTinNhanDenParent()">Thank you, My name is {{myName}}!</button>
  </div>
</template>

<!-- Javascript -->
<script>
export default {
  name: 'ChildComponent',
  data() {
    return {
      myName: 'Hieu'
    }
  },
  props: {
    yourName: String
  },
  methods: {
    guiTinNhanDenParent() {
      this.$emit('chaoLai', this.myName)
    }
  }
}
</script>

<!-- CSS -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
