/* eslint-disable */ 
<template>
    <div>
       
       <!-- <table border="0">

           <tr v-for="item in list" v-bind:key="item.id">
               <td>{{item.userId}}</td>
               <td>{{item.id}}</td>

               <td>{{item.title}}</td>
               <td>{{item.body}}</td>
           </tr>
       </table> -->
       <div class="container"  v-for="item in list" v-bind:key="item.id"  >
           <div class="content">User ID : {{item.userId}}</div>
           <div class="content" >Blog ID: {{item.id}}</div>
           <div class="content-2">{{item.title}}</div>
           <div class="content-2">{{item.body}}  <router-link :to="{ name: 'details', params: { id: item.id } }" >Show details</router-link></div>
          
       </div>
      
   </div>

</template>

<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)
export default {
    name: "ContentComponent",
   data(){
    return {
        list:"Hi",
       
        
    }
   },
    mounted() {
        Vue.axios.get(' https://jsonplaceholder.typicode.com/posts ')
            .then((resp) => {
                this.list = resp.data;
                console.warn(resp.data)
                             })
               },
    
            }
    


</script>

<style>
*{
    text-align: justify;
    padding: 1%;
}
.container{
    background-color:#23689B;
    
}
.content{
    background-color: white;
}
.content-2{
    background-color:#D6E0F0;
}

</style>