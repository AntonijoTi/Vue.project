<template>
   <div class="q-pa-md">
      <div class="text-h5 q-pa-md">NAUJAUSIOS</div>

        <q-scroll-area
          :thumb-style="thumbStyle"
          :bar-style="barStyle"
          :visible="true"
          style="height: 400px; max-width: 300px;"
        >

        <div class="contanier" ref="test">
    <ul>
      {{articles}}
      <li v-for="n in 20" :key="n" class="q-pa-xs" style=" list-style-type: none;">
      <span class="text-weight-medium ">14:13</span>
      <a href="https://www.krepsinis.net/" style="text-decoration: none; color: inherit;" class="text-body1" >
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Distinctio, porro?</a>
      </li>
    </ul>
  </div>

        </q-scroll-area>
    </div>
</template>

<script>
import { defineComponent } from 'vue';
import axios from 'axios';

export default defineComponent({
  name: 'ScrollArea',
  data() {
    return {
      articles: [],
    };
  },
  props: {
    title: {
      type: String,
    },
    href: {
      type: String,
    },
  },
  mounted() {
    axios('https://un4szcmf.directus.app/items/article')
      .then((response) => {
        console.log(response);
        this.articles = response.data.data;
      });
  },
  setup() {
    return {
      thumbStyle: {
        borderRadius: '0px',
        backgroundColor: '#007cc3',
        width: '6px',
        opacity: 1,
      },
      barStyle: {
        borderRadius: '0px',
        backgroundColor: '#e7e6e6',
        width: '6px',
        opacity: 1,
      },
    };
  },
});
</script>
