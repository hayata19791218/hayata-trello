<template>
    <form 
        @submit.prevent="addList" 
        class="addlist"
    >
        <input 
            type="text" 
            class="text-input"
            v-modle="title"
            placeholder="Add new list"
        >
        <button 
            class="add-button"
            type="submit"
        >
            Add
        </button>
    </form>
</template>

<script>
export default{
    data:function(){
        return{
            title:''
        }
    },
    methods:{
        addList:function(){
            this.$store.dispatch('addlist',{title:this.title})
            this.title=''
        }
    }
}
</script>