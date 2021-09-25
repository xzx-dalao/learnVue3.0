<template>
  <div>
        <p>{{ age}}</p>
    <button @click="myfn2">++</button>
  </div>
</template>

<script>
//ref的本质还是reacive
//reactive还是个对象，通过。value来修改
//template中不用添加。value,会自动添加
import {ref} from 'vue'
export default {
  name: "",
  setup() {
      let age=ref(18)
      function myfn2(){
         age.value=666
         console.log(age)
      }
      return {myfn2,age}
  },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>