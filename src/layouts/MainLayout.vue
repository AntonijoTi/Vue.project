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
    <div
      style="max-width: 800px; margin: auto;"
     >
       <div class="row justify-center" >
          <div class="col-8">
        <SmallCard
          photo="fbbc0e93-527d-4ac4-a211-bc8cecd2e754"
        />
          </div>
      <!-- Scrolll area -->
          <div class="col-4">
        <ScrollArea
        title="ScrollBar"
        />
          </div>
        </div>
          <!-- <q-separator/> -->
          <!--  Cards (two in line) -->
          <div class="row justify-center">
      <div v-for="a in cards" :key="a" class="col-md-6">
        <SmallCard style="border-top: 1px solid gray;"
          :title="a.title"
          :author="a.author"
          :photo="a.photo"
          :link="a.link"
        />
      </div>
    </div>
  </div>
  <!-- Empty Area -->
      <div class="col-4">
      </div>
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
