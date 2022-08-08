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
      <li v-for="a in articles" :key="a" class="q-pa-xs" style=" list-style-type: none;">
      <span class="text-weight-medium ">{{ a.datetime }}</span>
      <a  style="text-decoration: none; color: inherit;" :href="a.url"> {{ a.Title }}  </a>
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
    url: {
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
