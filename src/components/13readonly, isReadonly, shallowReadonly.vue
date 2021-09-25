<template>
  <div>
    <p>{{ state.name }}</p>
    <p>{{ state.arr.age }}</p>
    <p>{{ state.arr.sex }}</p>
    <button @click="myfun">+++</button>
  </div>
</template>

<script>
import { readonly, isReadonly, shallowReadonly } from "vue";
//readonly :创建只读的数据，递归
//shallowReadonly：读取第一个数据，不递归
//const和readonly的区别：

export default {
  name: "",
  setup() {
    let state = shallowReadonly({ name: "ljj", arr: { age: 19, sex: 12 } });
    const value={name:'zs',age:123}
    function myfun() {
      state.name = "eee";
      state.arr.age = 11;
      state.arr.sex = 11;
      console.log(state);
     console.log(isReadonly(state)); 
    //结果是const修改了
      value.name='ls'
      value.age=456
      console.log(value)
    }
    return { state, myfun };
  },
};
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>