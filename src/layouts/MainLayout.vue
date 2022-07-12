<template>
  <div margin="100px">
    <q-toolbar class="bg-light-blue-7 text-white shadow-2 rounded-borders">
     <div><a href="/">
      <img src="../assets/icon_logo_ukraina.png" alt="logo" style="width: 190px" >
      </a>
      </div>
        <MenuButtons />
    </q-toolbar>
       </div>
       <div>
        <SmallCard
          title="olololo"
          img="https://static3.krepsinis.net/Uploads/Static/Images/680x434/3/77/c0/13/77c013209c649f548774e759a340b608.jpg?v=3.00.126&t=cr&s=680x434&m=3&f=/Uploads/UArticles/leadPhotos/6e/9a/cb/1a/6e9acb1a5b5a31005650656ad5e519d6.jpg"
        />
        <SmallCard
          title="olololo"
          img="https://static2.krepsinis.net/Uploads/Static/Images/680x434/3/a6/27/d3/a627d337412fe304d03b37e51fd72ec5.jpg?v=3.00.126&t=cr&s=680x434&m=3&f=/Uploads/UArticles/leadPhotos/e3/9e/c0/88/e39ec08858d9938b3717ac4f3f4c1a45.jpg"
        />
       </div>
       <ScrollArea title="ScrollBar"/>
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
