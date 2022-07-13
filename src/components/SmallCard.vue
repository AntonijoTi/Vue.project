<template>

  <div class="q-pa-md row items-start ">
    <q-card class="my-card shadow-0">
        <img :src="img">
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
