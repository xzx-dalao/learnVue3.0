<template>
<div>
<p>{{state}}</p>
<button @click="myfun">++</button>
</div>
</template>

<script>
//ref修改数据不会影响原来数据，会触发更新
//toRefs修改多个对象数据会影响原来数据，不会触发更新
import {ref,toRefs} from 'vue'
export default {
name:'', 
setup(){
    let obj={name:'xzx',age:19}
    let state=toRefs(obj)
    function myfun(){
        
        state.name.value='eee'
        state.age.value=213
        console.log(obj)
        console.log(state)

    }
    return {state,myfun}
}
}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>