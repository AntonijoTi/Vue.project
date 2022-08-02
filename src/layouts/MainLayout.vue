<template>
  <div margin="100px">
    <!--  Menu  -->
    <q-toolbar class="bg-light-blue-7 text-white shadow-2 rounded-borders">
      <!--   Menu  icon -->
      <div>
        <a href="/">
          <img src="../assets/icon_logo_ukraina.png" alt="logo" style="width: 190px" >
        </a>
        <!--   Menu buttons   -->
        <MenuButtons />
      </div>
    </q-toolbar>
    <!--  Cards (one card and one scroll) -->
    <div class="row justify-center" >
      <div class="col-6">
        <SmallCard
          photo="9781d3d7-8f7d-46e3-97f9-feaa525363cd"
        />
      </div>
      <!-- Scrolll area -->
      <div class="col-4">
        <ScrollArea
        title="ScrollBar"
        />
      </div>
    </div>
    <q-separator style='margin-right: 100px; margin-left: 100px'/>
    <!--  Cards (two in line) -->
    <div class="row justify-center ">
      <div v-for="a in cards" :key="a" class="col-6">
        <SmallCard
          :title="a.title"
          :author="a.author"
          :photo="a.photo"
        />
      </div>
    </div>
  </div>
  <!-- Empty Area -->
      <div class="col-4">
      </div>
 </template>

<script>
import { defineComponent } from 'vue';
import axios from 'axios';
import MenuButtons from '../components/MenuButtons';
import SmallCard from '../components/SmallCard';
import ScrollArea from '../components/ScrollArea';

export default defineComponent({
  name: 'MainLayout',
  data() {
    return {
      cards: [],
    };
  },

  components: {
    MenuButtons,
    SmallCard,
    ScrollArea,
  },
  mounted() {
    axios('https://un4szcmf.directus.app/items/Card')
      .then((response) => {
        console.log(response);
        this.cards = response.data.data;
      });
  },
  setup() {
    return {

    };
  },
});

</script>
