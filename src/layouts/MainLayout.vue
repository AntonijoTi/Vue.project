<template>
  <div class="q-pa-md">
    <q-toolbar class="bg-primary text-white">
      <q-btn flat round dense icon="menu" class="q-mr-sm" />
      <q-avatar>
        <img src="https://cdn.nba.com/logos/leagues/logo-nba.svg">
      </q-avatar>
      <q-btn flat @click="drawer = !drawer" round dense  label="Basic Menu">
        <q-menu>
          <q-list style="min-width: 100px">
            <q-item clickable v-close-popup>
              <q-item-section>New tab</q-item-section>
            </q-item>
            <q-item clickable v-close-popup>
              <q-item-section>New incognito tab</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Recent tabs</q-item-section>
            </q-item>
            <q-item clickable v-close-popup>
              <q-item-section>History</q-item-section>
            </q-item>
            <q-item clickable v-close-popup>
              <q-item-section>Downloads</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Settings</q-item-section>
            </q-item>
            <q-separator />
            <q-item clickable v-close-popup>
              <q-item-section>Help &amp; Feedback</q-item-section>
            </q-item>
          </q-list>
        </q-menu>
      </q-btn>
      <q-toolbar-title></q-toolbar-title>

      <q-btn flat round dense >Sign in</q-btn>
    </q-toolbar>
    <q-drawer
        v-model="drawer"
        :width="200"
        :breakpoint="500"
        overlay
        bordered
        class="bg-grey-3"
      >
        <q-scroll-area class="fit">
          <q-list>

            <template v-for="(menuItem, index) in menuList" :key="index">
              <q-item clickable :active="menuItem.label === 'Outbox'" v-ripple>
                <q-item-section avatar>
                  <q-icon :name="menuItem.icon" />
                </q-item-section>
                <q-item-section>
                  {{ menuItem.label }}
                </q-item-section>
              </q-item>
              <q-separator :key="'sep' + index" v-if="menuItem.separator" />
            </template>

          </q-list>
        </q-scroll-area>
      </q-drawer>
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue';
// import EssentialLink from 'components/EssentialLink.vue';
const menuList = [
  {
    icon: 'inbox',
    label: 'Inbox',
    separator: true,
  },
  {
    icon: 'send',
    label: 'Outbox',
    separator: false,
  },
  {
    icon: 'delete',
    label: 'Trash',
    separator: false,
  },
  {
    icon: 'error',
    label: 'Spam',
    separator: true,
  },
  {
    icon: 'settings',
    label: 'Settings',
    separator: false,
  },
  {
    icon: 'feedback',
    label: 'Send Feedback',
    separator: false,
  },
  {
    icon: 'help',
    iconColor: 'primary',
    label: 'Help',
    separator: false,
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    // EssentialLink,
  },

  setup() {
    return {
      tab: ref('mails'),
      drawer: ref(true),
      menuList,
    };
  },
});

</script>
