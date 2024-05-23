<template>
  <div class="sidebar" :class="{'active':props.menuOpen}">
<!--    <span class="material-symbols-outlined close-icon">close</span>-->
    <div class="logo"><b>CRM.io</b></div>
    <PerfectScrollbar class="scroll-area">
      <ul class="menu">
        <li><a href="" class="active"><span class="material-symbols-outlined">dashboard</span>Dasboard</a></li>
        <li>
          <span class="submenu">Managment</span>
          <ul>
            <li><a href=""><span class="material-symbols-outlined">folder_open</span>Document</a></li>
            <li><a href=""><span class="material-symbols-outlined">contact_support</span>Contact</a></li>
            <li><a href=""><span class="material-symbols-outlined">psychology</span>Prospect</a></li>
            <li><a href=""><span class="material-symbols-outlined">rebase</span>Workflow</a></li>
          </ul>
        </li>

        <li>
          <span class="submenu">Connection</span>
          <ul>
            <li><a href=""><span class="material-symbols-outlined">headset_mic</span>Chat Integration</a></li>
            <li><a href=""><span class="material-symbols-outlined">linked_services</span>Marketing Automation</a></li>
            <li><a href=""><span class="material-symbols-outlined">email</span>Email Integration</a></li>
          </ul>
        </li>

        <li>
          <span class="submenu">Connection</span>
          <ul>
            <li><a href=""><span class="material-symbols-outlined">headset_mic</span>Chat Integration</a></li>
            <li><a href=""><span class="material-symbols-outlined">linked_services</span>Marketing Automation</a></li>
            <li><a href=""><span class="material-symbols-outlined">email</span>Email Integration</a></li>
          </ul>
        </li>

        <li>
          <span class="submenu">Connection</span>
          <ul>
            <li><a href=""><span class="material-symbols-outlined">headset_mic</span>Chat Integration</a></li>
            <li><a href=""><span class="material-symbols-outlined">linked_services</span>Marketing Automation</a></li>
            <li><a href=""><span class="material-symbols-outlined">email</span>Email Integration</a></li>
          </ul>
        </li>

      </ul>
    </PerfectScrollbar>
  </div>


</template>

<script>
import { PerfectScrollbar } from 'vue3-perfect-scrollbar';
import 'vue3-perfect-scrollbar/style.css';
export default {
  name: "TheSidebar",
  props: ['menuOpen'],
  components: {
    PerfectScrollbar,
  },
  setup(props){
    return {
      props
    }

  }
}
</script>

<style>
.ps .ps__rail-x:hover, .ps .ps__rail-y:hover, .ps .ps__rail-x:focus, .ps .ps__rail-y:focus, .ps .ps__rail-x.ps--clicking, .ps .ps__rail-y.ps--clicking{
  background: rgba(33, 28, 102, 0.83) !important;
}

</style>