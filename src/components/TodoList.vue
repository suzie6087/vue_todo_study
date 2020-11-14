<template>
    <div></div>
</template>

<script>
export default {
    data:function() {
        return {
            todoItems:[]
        }
    },
    /* life cycle method */
    created:function() {
        if(localStorage.length > 0){
            for(var i=0 ; localStorage.length ; i++){
                this.todoItems.push(localStorage.key(i));
            }
        }
    }
}
</script>

<style>
</style>
