<template>
<div>
{{state}}
<button @click="myfun">++</button>
</div>
</template>

<script>
//ref和react都会跟踪，消耗性能
//toraw可以拿到原始数据
import {reactive,toRaw} from 'vue'
export default {
name:'', 
setup(){
let obj={name:'xzx',age:18}
let state=reactive(obj)
let obj2=toRaw(state)
console.log(obj===obj2)
function myfun(){
    obj2.name='eee'
}
return {state,myfun}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>