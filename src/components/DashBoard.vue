
<script>

import { ref } from 'vue'
import Card from  "./TheCard.vue";
import GraphCard from "./GraphCard.vue";
import TableCard from "./TableCard.vue";
import RightBar from "./RightBar.vue";


export default {
  name: "DashBoard",
  components: {
    GraphCard,
    TableCard,
    Card,
    RightBar
  },


  setup(){
    const objCard = ref([
      {
        type:'card',
        title:'Document',
        icon:'description',
        description:'177.555',
        ratio:'10',

      },
      {
        type:'card',
        title:'Contact',
        icon:'phone_in_talk',
        description:'1400',
        ratio:'90',

      },
      {
        type:'card',
        title:'Email',
        icon:'mail',
        description:'170.555',
        ratio:'12',

      }
    ]);


    const objTable = ref(
        [
          {
            type:'table',
            title:'Document',
            icon:'',
            description:'Document Tracking Information',
            data:[
              {
                name:'Annual Report',
                file:'PDF',
                category:'Property',
                author:'Diana',
                status:'Send',

              },
              {
                name:'Business Plan',
                file:'PDF',
                category:'Crypto',
                author:'James',
                status:'Send',

              },
              {
                name:'Marketing Tool',
                file:'Word',
                category:'Property',
                author:'Andy',
                status:'pending',

              }
            ]
          }],
    );

    return {
      objCard,
      objTable
    };

  }

}
</script>
<template>
  <div class="content">
    <h1 class="mb-20">Overview</h1>
    <div class="container">
      <div class="row">
        <div class="col-9">
          <card  v-if="objCard" :obj="objCard"/>
          <graph-card/>
          <table-card v-if="objTable" :obj="objTable"/>
        </div>
        <div class="col-3">
          <div class="container">
            <div class="col-12" >
              <RightBar/>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

</template>


<style scoped>

</style>