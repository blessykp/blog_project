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
        <div class="container"  v-for="item in list" v-bind:key="item.id">
            <div class="content">{{item.userId}}{{item.id}}</div>
            <div class="content">{{item.title}}</div>
            <div class="content">{{item.body}}</div>
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
        list:"Hi"
    }
   },
    mounted() {
        Vue.axios.get(' https://jsonplaceholder.typicode.com/posts ')
            .then((resp) => {
                this.list = resp.data;
                console.warn(resp.data)
                             })
               }
            }


</script>

<style>
*{
    text-align: justify;
    padding: 1%;
}
.container{
    background-color: cadetblue;
    
}
.content{
    background-color: white;
}

</style>