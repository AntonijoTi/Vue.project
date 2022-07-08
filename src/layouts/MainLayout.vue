<template>
  <div margin="100px">
    <q-toolbar class="bg-light-blue-7 text-white shadow-2 rounded-borders">
     <div><a href="/">
      <img src="../assets/icon_logo_ukraina.png" alt="logo" style="width: 190px" >
      </a>
     </div>
     <MenuButtons/>
    </q-toolbar>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import { MenuButtons } from '../components/MenuButtons';

export default defineComponent({
  name: 'MainLayout',

  components: {
    MenuButtons,
  },

  setup() {
    return {
      lorem: '„Shaqtin\' A Fool“ – nepavykusi J.Valančiūno bendraklubio afera ir „Nets“ nesusipratimas',
    };
  },
});

</script>
