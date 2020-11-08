<template>
    <div>
        <input type="text" v-model="newTodoItem">
        <button v-on:click="addTodo">추가</button>
    </div>
</template>

<script>
export default {
   methods:{
       addTodo: function(){
           console.log(this.newTodoItem);
       }
   }
}
</script>

<style>
</style>
