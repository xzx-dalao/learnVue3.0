<template>
  <div>
    <ul>
      <li
        v-for="(item, index) in state.stus"
        :key="index"
        @click="remove(index)"
      >
        {{ item.name }}
      </li>
    </ul>

    <input type="text" v-model="state2.stu2.name">
    <input type="submit" @click="add">
  </div>
</template>

<script>
import { reactive } from "vue";
export default {
  name: "ee",
  setup() {
    let { state, remove } = userstu();
    let  {add,state2} = userAdd(state)
     return { state, remove,state2,add};
  },
};
function userstu() {
  let state = reactive({
    stus: [
      {
        name: "eee",
      },
      {
        name: "heuwahieu",
      },
    ],
  });
  function remove(index) {
    state.stus = state.stus.filter((stu, idx) => idx !== index);
  }
  return { state, remove };
}
function userAdd(state) {
        let state2= reactive({
        stu2:{
            name:''
        }
    })
    function add(e) {
        e.preventDefault()
        const stu=Object.assign({},state2.stu2)
        state.stus.push(stu)
        state2.stu2.name=''
    }
    return {add,state2}
}
</script>
<style scoped>
/* @import url(); 引入css类 */
</style>