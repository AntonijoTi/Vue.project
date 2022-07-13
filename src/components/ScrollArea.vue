<template>
<div class="q-ma-md">
        <q-scroll-area
          :thumb-style="thumbStyle"
          :bar-style="barStyle"
          :visible="true"
          style="height: 400px; max-width: 300px;"
        >
          <div v-for="n in 1000" :key="n" class="q-pa-xs">
            <div>
              <a
                href=""
                style="text-decoration: none;">
                basketball
              </a>
            </div>
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
