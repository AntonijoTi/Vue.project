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
    <div class="row justify-center">
      <div class="col-4">
        <SmallCard
          title="olololo"
          img="https://static2.krepsinis.net/Uploads/Static/Images/680x434/3/02/23/8d/02238d49420b48eb02bc7320186ade05.jpg?v=3.00.126&t=cr&s=680x434&m=3&f=/Uploads/UArticles/leadPhotos/7a/7a/3a/ea/7a7a3aeaecf8a9359693bc57198aae9f.jpg"
        />
      </div>
      <!-- Scrolll area -->
      <div class="col-4">
        <ScrollArea title="ScrollBar"/>
      </div>
    </div>
    <!--  Cards (two in line) -->
    <div class="row justify-center">
      <div class="col-2" style="max-width: 400px">
        <SmallCard
          title="olololo"
          img="https://static3.krepsinis.net/Uploads/Static/Images/680x434/3/77/c0/13/77c013209c649f548774e759a340b608.jpg?v=3.00.126&t=cr&s=680x434&m=3&f=/Uploads/UArticles/leadPhotos/6e/9a/cb/1a/6e9acb1a5b5a31005650656ad5e519d6.jpg"
        />
      </div>
      <div class="col-2" style="max-width: 400px">
        <SmallCard
          title="olololo"
          lass="col col-md-4"
          img="https://static2.krepsinis.net/Uploads/Static/Images/680x434/3/a6/27/d3/a627d337412fe304d03b37e51fd72ec5.jpg?v=3.00.126&t=cr&s=680x434&m=3&f=/Uploads/UArticles/leadPhotos/e3/9e/c0/88/e39ec08858d9938b3717ac4f3f4c1a45.jpg"
        />
      </div>
      <!-- Empty Area -->
      <div class="col-4">
      </div>
    </div>
  </div>
 </template>

<script>
import { defineComponent } from 'vue';
import MenuButtons from '../components/MenuButtons';
import SmallCard from '../components/SmallCard';
import ScrollArea from '../components/ScrollArea';

export default defineComponent({
  name: 'MainLayout',

  components: {
    MenuButtons,
    SmallCard,
    ScrollArea,
  },

  setup() {
    return {

    };
  },
});

</script>
