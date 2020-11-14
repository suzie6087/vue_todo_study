<template>
    <div class="inputBox shadow">
        <input type="text" v-model="newTodoItem" v-on:keyup.enter="addTodo">
        <button v-on:click="addTodo">추가</button>
    </div>
</template>

<script>
export default {
   methods:{
       addTodo: function(){
           // input이 비어있지 않는다면 
           if(this.newTodoItem !== ''){
               // 입력받은 텍스트를 localStorage에 저장한다. 
               localStorage.setItem(this.newTodoItem, this.newTodoItem);
               // addTodo 해주고 나서 input창 clear해주는 fn 
               this.clearInput();
           }
       },
       clearInput: function() {
           console.log("sss");
            this.newTodoItem = '';
       }
   }
}
</script>

<style>
input:focus{
    outline:none;
}
.inputBox{
    background:white;
    height:50px;
    line-height:50px;
    border-radius:5px;
}
.inputBox input{
    border-style:none;
    font-size: 0.9rem;
}
.addContainer{
    float:right;
    background:linear-gradient(to right, #6478FB, #8763FB);
    display:block;
    width:3rem;
    border-radius:0 5px 5px 0;
}
.addBtn{
    color:white;
    vertical-align:middle;
}
</style>
