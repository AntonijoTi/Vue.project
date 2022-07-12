<template>

  <div class="q-pa-md row items-start " style="margin:0
  ">
    <q-card class="my-card" >
        <img :src="img" style=" margin: 0px auto" >
      <q-card-section>
        <div class="text-h12">
        </div>
        <div class="text-subtitle2">by John Doe</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
    </q-card>
</div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'SmallCard',
  props: {
    title: {
      type: String,
    },
    img: {
      type: String,
    },
  },

  setup() {
    return {
      lorem: '„Shaqtin\' A Fool“ – nepavykusi J.Valančiūno bendraklubio afera ir „Nets“ nesusipratimas',
    };
  },
});
</script>
