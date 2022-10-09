<template>
    <div class="hook">
        <h1>{{title}}</h1>
        <button v-on:click="changeTitle">Click me</button>
    </div>
</template>

<script>
export default {
    name:'hook',
    data(){
        return {
            title: 'Hook part'
        }
    },
    methods:{
        changeTitle(){
             this.title = 'shahidul islam'
        }
    },
    // beforeUpdate(){
    //     alert('befor update')
    // },

    // beforeCreate(){
    //     alert('before created hook')
    // },
    // created(){
    //     alert('create hook') 
    // },
    // beforeMount(){
    //     alert('before mounted hook')
    // },
    // mounted(){
    //     alert('mounted hook')

    // }
}
</script>

<style scoped>

</style>> 
