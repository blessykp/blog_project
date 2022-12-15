<template>
    <div class="container">
      

      
        <div class="content">{{ list[item-1].userID}}</div>
        <div class="content">{{list[item-1].id }}</div>
        <div class="content">{{ list[item-1].title }}</div>
        <div class="content">{{ list[item-1].body}}</div>
    </div>


</template>
<script>
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
Vue.use(VueAxios, axios)


export default {
    name: "DetailsComponent",
    data() {
        return {
            list: "",
            item:this.$route.params.id,
            el:""
        }
    },
    props:{
        
    },

mounted() {
    // let blog_id=this.$route.params.id
    Vue.axios.get('https://jsonplaceholder.typicode.com/posts/')
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
    background-color: cadetblue;
    
}
.content{
    background-color: white;
}
</style>