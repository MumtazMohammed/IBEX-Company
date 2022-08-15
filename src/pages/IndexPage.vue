<template>
  <q-page class="row items-center justify-start">
    <q-avatar square size="500px">
      <q-img src="../assets/ibex-l-g-01.png" contain spinner-color="red" />
    </q-avatar>
    <p>Coming soon</p>
  </q-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  components: {},
  setup() {
    return {};
  },
});
</script>
<style lang="scss" scoped>
.q-page {
  background-color: $Y;
  flex-direction: column;
  font-family: sans-serif;
}
p {
  font-family: serif;
  font-size: 25px;
  letter-spacing: 1.5px;
  font-weight: 700;
}
</style>
