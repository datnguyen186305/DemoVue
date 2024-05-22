<!-- HTML -->
<template>
  <div>
    <p>Welcome {{ten}} !</p>
    <ChildComponent :yourName="ten" @chaoLai="hienThiTenCon"></ChildComponent>
  </div>
</template>

<!-- Javascript -->
<script>
import ChildComponent from "@/components/ChildComponent.vue";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Parent',
  components: {ChildComponent},
  props: {
    ten: String
  },
  methods: {
    hienThiTenCon(ten) {
      alert('Chao ' + ten);
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
