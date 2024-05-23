<template>
  <div class="navbar">
    <span class="material-symbols-outlined menu" @click="menuOpen">{{ isMenuOpened ? 'close' : 'menu'}}</span>

    <ul class="navbar-wrap">
        <li>
          <span class="material-symbols-outlined">notifications</span>
        </li>
        <li>
          <a class="dropdown-toggle">
            <img src="../../assets/profile.jpeg" alt="">
            <span class="mr-5">Administrator</span>
            <span class="material-symbols-outlined icon">expand_more</span>
          </a>
        </li>
    </ul>
  </div>
</template>

<script>
import {ref} from 'vue';
export default {
  emits:["isMenuOpened"],
  name: "TheNavbar",
  setup(_, context){
    const isMenuOpened = ref(false)
    function menuOpen () {
      isMenuOpened.value = !isMenuOpened.value;
      context.emit('isMenuOpened',this.isMenuOpened)
    }
    return {
      isMenuOpened,
      menuOpen
    }
  }
}
</script>

<style scoped>

</style>