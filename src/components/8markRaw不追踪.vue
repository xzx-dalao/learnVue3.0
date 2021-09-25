<template>
<div>
{{state}}
<button @click="myfun">++</button>
</div>
</template>

<script>

//markRaw不被追踪，ui不会更新
import {reactive,markRaw} from 'vue'
export default {
name:'', 
setup(){
let obj={name:'xzx',age:18}
obj=markRaw(obj)
let state=reactive(obj)

console.log(obj===obj2)
function myfun(){
    state.name='eee'
}
return {state,myfun}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>