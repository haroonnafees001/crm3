<template>
  <div>
    <Navbar  @isMenuOpened="isMenuOpened"/>
    <Sidebar :menuOpen="isMenuActive"/>
  </div>

</template>


<script>

import Sidebar from './header/TheSidebar.vue'
import Navbar from './header/TheNavbar.vue'
import { ref } from 'vue'
export default {
  name: "TheHeader",
  components: {
    Sidebar,
    Navbar
  },
  setup(){
    const isMenuActive = ref(false)
     function isMenuOpened (event) {
      isMenuActive.value = event;
     }
    return {
      isMenuOpened,isMenuActive
    }
  }

}
</script>

<style scoped>

</style>