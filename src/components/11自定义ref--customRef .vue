<template>
<div>
    <p>{{age}}</p>
    <button @click="myfun">++</button>
</div>
</template>

<script>
import {customRef} from 'vue'
export default {
name:'', 
setup(){
let age=myref(10)
function myfun(){
    age.value+=1
}
return {age,myfun}
}

}
function myref(value){
    return customRef((track, trigger)=>{
        return{
            get(){
                track()//告诉vue这个数据是要追踪的
                // console.log(value)
                return value
            },
            set(newvalue){
               
                // console.log(newvalue)
                value=newvalue
                trigger()//告诉vue这个数据是要触发更新的
            } 
        }
    })


}
</script>
<style scoped>
/* @import url(); 引入css类 */

</style>