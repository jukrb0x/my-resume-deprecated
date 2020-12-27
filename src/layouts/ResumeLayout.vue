<template>
  <q-layout view="hHh lpR fFf">
    <q-page-container class="cv">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  data() {
    return {};
  }
};
</script>

<style lang="sass" scoped>
.cv
  display: flex
  justify-content: center
  align-items: center
  background: #f6f6f6
</style>
