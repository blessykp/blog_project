<template>
  <div class="home">
   
   
    <HeaderComponent/>
    <ContentComponent></ContentComponent>
    <FooterComponent/>
      </div>
</template>

<script>
// @ is an alias to /src

import HeaderComponent from '@/components/HeaderComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
import ContentComponent from '@/components/ContentComponent.vue'
export default {
  name: 'HomeView',
  components: {
   HeaderComponent,
   FooterComponent,
   ContentComponent,
  }
}
</script>
