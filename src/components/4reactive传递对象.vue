<template>
<div>
<p>{{state.age}}</p>
<button @click="myfun">myfun</button>
<p>{{state2}}</p>
<button @click="myfun2">myfun2</button>
</div>
</template>

<script>
//reactive 传递的是对象(json/arr)
//如果是其他对象必须重新赋值
import {reactive} from 'vue'
export default {
name:'', 
setup(){
let state=reactive({
    age:123
});

function myfun(){
    state.age=666
 console.log(state)
}
let state2=reactive([1,2,3]);
function myfun2(){
    state2[0]=555
}
return {myfun,state,state2,myfun2}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>