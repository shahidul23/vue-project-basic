<template>
    <div id="onlinefriends">
        <h2>Online Frienda list</h2>
        <div v-for="(friend,index) in friends" :key="index">
            <h3 v-if="friend.status">{{friend.name}}</h3>
        </div>

    </div>
</template>

<script>
export default {
    name:'OnlineFriends',
     props:['friends'],
    data(){
        return {
            
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
