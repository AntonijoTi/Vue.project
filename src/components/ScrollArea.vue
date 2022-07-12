<template>
<div class="q-ma-md">
        <q-scroll-area
          :thumb-style="thumbStyle"
          :bar-style="barStyle"
          style="height: 200px; max-width: 300px;"
        >
          <div v-for="n in 100" :key="n" class="q-pa-xs">
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          <div><a href="">basketball</a></div>
          </div>
        </q-scroll-area>
    </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ScrollArea',
  props: {
    title: {
      type: String,
    },
  },

});
</script>
