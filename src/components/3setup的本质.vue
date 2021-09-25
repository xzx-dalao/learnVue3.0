<template>
  <div>
    <p>{{ name }}</p>
    <button @click="myfn1">++</button>
        <p>{{ age}}</p>
    <button @click="myfn2">++</button>
  </div>
</template>

<script>
import {ref} from 'vue'
export default {
  name: "",
  data() {
    return {
      name: "xzx",
    };
  },
  methods: {
    myfn1() {
      alert("666");
    },
  },
  setup() {
      let age=ref(18)
      function myfn2(){
          alert('777')
      }
      return {myfn2,age}
  },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>