<template>
  <div>
    <q-btn stretch flat label="Naujienos">
      <q-menu
        transition-show="jump-up"
        transition-hide="jump-down"
      >
        <q-list style="min-width: 100px">
          <q-item clickable>
            <q-item-section>Olimpiada</q-item-section>
          </q-item>
          <q-item clickable>
            <q-item-section>Crazy for transitions</q-item-section>
          </q-item>
          <q-separator />
          <q-item clickable>
            <q-item-section>Mind blown</q-item-section>
          </q-item>
        </q-list>
      </q-menu>
    </q-btn>

    <q-btn stretch flat label="Menedžeris">
      <q-menu
        transition-show="jump-up"
        transition-hide="jump-down"
      >
        <q-list style="min-width: 100px">
          <q-item clickable>
            <q-item-section>Having fun</q-item-section>
          </q-item>
          <q-item clickable>
            <q-item-section>Crazy for transitions</q-item-section>
          </q-item>
          <q-separator />
          <q-item clickable>
            <q-item-section>Mind blown</q-item-section>
          </q-item>
        </q-list>
      </q-menu>
    </q-btn>

    <q-btn stretch flat label="Registruotis" />
    <q-btn stretch flat :label="title" />
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MenuButtons',
  props: {
    title: {
      type: String,
    },
  },
});
</script>
