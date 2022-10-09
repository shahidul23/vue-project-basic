<template>
    <div>
        <h1>posts</h1><hr>
        <input type="text" v-model="searchTerm">
        <div v-for="(post) in searchFilter" :key="post.id">
         <h2>{{post.title | title}}</h2>
         <p>{{post.body | snippet}}</p><hr>
        
        </div>
    </div>
</template>

<script>
import axios from'axios'
export default {
    name:'axios',
    data(){
        return{
            posts:[],
            searchTerm:''

        }
    },
    computed:{
        searchFilter(){
          return this.posts.filter(post =>{
                return post.title.match(this.searchTerm)
            })
        }
    },
    created(){
        axios.get('https://jsonplaceholder.typicode.com/posts')
        .then(response =>{
            //console.log(response)
            this.posts = response.data

        })      .catch(error =>{ 
            console.log(error)
        })
    }
}
</script>

<style scoped>

</style>