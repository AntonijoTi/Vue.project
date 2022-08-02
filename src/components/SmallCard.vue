<template>

  <div class="q-pa-lg items-start ">
    <q-card class="my-card shadow-0">
        <img :src="'https://un4szcmf.directus.app/assets/' + photo">
      <q-card-section>
        <div class="text-h12">
        </div>
        <div class="text-subtitle2"> {{ author }}</div>
      </q-card-section>
        <q-card-section class="q-pt-none">
        {{ title }}
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
    author: {
      type: String,
    },
    photo: {
      type: String,
    },
    datetime: {
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
