<template>
    <div id="allfriends">
        <h2>All Frienda list</h2>
            <div v-for="(friend,index) in friends" v-bind:key="index"> 
            <h2 @click="unfriend(friend.name)">{{friend.name}}</h2>
            </div>
    </div>
</template>

<script>
export default {
    name:'AllFriends',
    props:['friends'],
    data(){
        return {
           
        }
    },
    methods:{
        unfriend(name){
            this.$emit('delete',{name})
        }
    }
    
}
</script>

<style scoped>
nav{
    text-align: center;
}
nav ul{
    padding: 0;
}
nav li{
    padding: 8px;
    margin: 0;
    display: inline-block;
    list-style-type: none;
    
}

</style>
