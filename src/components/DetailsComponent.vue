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
           <div class="content">{{item.userId}}</div>
           <div class="content" v-bind="blogid" @click="detail(item.id)">{{item.id}}</div>
           <div class="content">{{item.title}}</div>
           <div class="content">{{item.body}}</div>
       </div>
      
   </div>
</template>
<script>

</script>

<style>

</style>