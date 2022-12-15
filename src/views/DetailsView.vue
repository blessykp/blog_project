<template>
  <div class="home">
   
   
    <HeaderComponent/>
    <DetailsComponent></DetailsComponent>
    <FooterComponent/>
      </div>
</template>

<script>
// @ is an alias to /src

import HeaderComponent from '@/components/HeaderComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
import DetailsComponent from '@/components/DetailsComponent.vue'
export default {
  name: 'HomeView',
  components: {
   HeaderComponent,
   FooterComponent,
   DetailsComponent
  }
}
</script>
