<template>
<div>
    <p>{{count}}</p>
<button @click="myfun">+</button>
</div>

</template>

<script>
import { ref } from "vue";
export default {
  name: "hellow",
  setup() {
      let count =ref(0)
      function myfun(){
          count.value+=1
      }
      return {count,myfun}
  },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>