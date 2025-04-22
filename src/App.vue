<template>

  <div id="main" class="box-border max-w-full h-screen text-white flex items-center">
    <div class=" max-w-full w-[90vw] h-[90vh] overflow-hidden mx-auto flex  lg:bg-gray-900/80 shadow-2xl rounded shadow-black">
      <!-- SideBar -->
      <Sidebar @tab-changed="handelCurrentlyActiveTab" />


      <!-- Hero -->
      <hero :tabNo="ChangedTabNo"></hero>




    </div>
  </div>

</template>

<script>

import Hero from './components/Hero.vue';
import Sidebar from './components/Sidebar/Sidebar.vue';

import 'primeicons/primeicons.css'

export default {
  components: {
    Sidebar,
    Hero
  },
  data() {
    return {
      // isRotated: "front",
      ChangedTabNo: '1',
      rotateY: 0
    };
  },
  methods: {
    handelCurrentlyActiveTab(no) {
      this.ChangedTabNo = no
      console.log("This is no value: " + no);
      console.log("this is tabNo value " + this.ChangedTabNo);
      
      
    }
  }

}
</script>


<style scoped>

#main{
background-image: url('./assets/Images/hero2.jpg');
background-position: center;
background-size: cover;
background-repeat: no-repeat;
}

</style>