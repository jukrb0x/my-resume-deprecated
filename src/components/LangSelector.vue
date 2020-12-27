<template>
  <q-btn-dropdown color="primary" size="sm" :label="currentLangName">
    <q-list>
      <q-item
        v-for="lang in langOptions"
        :key="lang.name"
        clickable
        v-close-popup
        @click="switchLang(lang.code)"
      >
        <q-item-section>
          <q-item-label>{{ lang.name }}</q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
  </q-btn-dropdown>
</template>

<script>
export default {
  name: 'LangSelector',
  props: ['currentLangCode', 'switchLang'],
  data() {
    return {
      langOptions: [
        {
          name: 'English',
          code: 'en-us'
        },
        {
          name: '简体中文',
          code: 'zh-cn'
        }
      ]
    };
  },
  computed: {
    currentLangName: function() {
      // get the name of lang code
      if (this.currentLangCode === 'en-us') {
        return 'English';
      }
      if (this.currentLangCode === 'zh-cn') {
        return '简体中文';
      }
    }
  },
  methods: {}
};
</script>

<style scoped></style>
