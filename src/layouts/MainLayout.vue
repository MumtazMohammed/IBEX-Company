<template>
  <q-layout view="hHh lpR fFf">
    <q-header reveal class="text-white q-py-xs">
      <q-toolbar>
        <q-btn  class="bg-white" flat round icon="menu" @click="toggleLeftDrawer" />
        <q-space />
        <q-avatar square size="80px">
          <img contain src="../assets/ibex-l-y-01.png" />
        </q-avatar>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" side="left" overlay behavior="desktop">
      <!-- drawer content -->
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal class="text-white">
      <q-toolbar>
        <q-toolbar-title>
          <div class="row justify-end">
            <small class=""> &COPY; IEBX FURNITURE </small>
          </div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
};
</script>
<style lang="scss" scoped>
.q-header {
  background-color: $G;
}
.q-footer {
  background-color: $G;
}
small {
  font-family: sans-serif;
  letter-spacing: 1px;
  font-size: 14px;
}
::v-deep.q-btn .q-icon {
  color: $Y;
  font-size: 28.2px;
}
</style>
