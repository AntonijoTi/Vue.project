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
          <a style="text-decoration: none; color: inherit;" :href="link">
        {{ title }}
        </a>
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
    link: {
      type: String,
    },
  },
  setup() {
    return {
    };
  },
});
</script>
