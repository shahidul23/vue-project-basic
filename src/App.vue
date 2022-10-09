<template>
  <div id="app">
    <h1>{{title}}</h1>
    <Navbar></Navbar>
    <AllFriends :friends="friends" @delete="deleteFriends"></AllFriends>
    <OnlineFriends :friends="friends"></OnlineFriends>
    <hook></hook>
    <axios></axios>
    
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import AllFriends from './components/AllFriends.vue'
import OnlineFriends from './components/OnlineFriends.vue'
import hook from './components/hook.vue'
import axios from './components/axios.vue'
export default {
  name: 'App',
  data(){
    return {
      title:'This is my vue js Project',
       friends:[
                {name:'A',status:true},
                {name:'B',status:true},
                {name:'C',status:false},
                {name:'D',status:true},
                {name:'E',status:false}
            ]
    }
  },
  components: {
      Navbar,
      AllFriends,
      OnlineFriends,
      hook,
      axios
  },
  methods:{
    deleteFriends(paylood){
      //console.log(paylood)
      this.friends = this.friends.filter(friend => {
          return friend.name !== paylood.name
      })
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
