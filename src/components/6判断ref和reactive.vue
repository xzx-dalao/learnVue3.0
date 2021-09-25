<template>
  <div>
    <p>
      {{ age }}
    </p>
    <p>
      {{ age2 }}
    </p>
    <button @click="myfun">++</button>
  </div>
</template>
<script>
//ref时候vue会自动添加.value
//reactive,不会自动添加.value
import { ref, reactive,isRef,isReactive} from "vue";
export default {
  name: "",
  setup() {
    let age = ref(1);
    let age2 = reactive({ value: 18 });
    function myfun(){
        console.log(isRef(age))
         console.log(isReactive(age2))
    }
    return { age, age2 ,myfun};
  },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>