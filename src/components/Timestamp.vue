<template>
  <div class="time-stamp">
    <div class="last-updated">Last updated: {{ date }}</div>
    <div class="copyright">
      <a href="https://github.com/jukrb0x" target="_blank">
        Follow me on <q-icon name="fab fa-github"></q-icon> Github
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'timestamp',
  data() {
    return {
      date: 'December 28, 2020'
    };
  }
};
</script>

<style lang="sass" scoped>
.time-stamp
  display: flex
  flex-direction: column
  justify-content: space-between
  align-items: center
  color: $grey
  .copyright a
    transition: .3s ease
    color: $grey
  .copyright a:hover
    color: #1D1D1D
</style>
