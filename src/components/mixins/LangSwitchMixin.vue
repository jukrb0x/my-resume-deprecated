<script>
export default {
  name: 'LangSwitchMixin',
  data() {
    return {
      currentLangCode: this.$i18n.locale
    };
  },
  methods: {
    switchLang(langCode) {
      // switch the current language code and app i18n code
      this.currentLangCode = langCode;
      this.$i18n.locale = langCode;
      // it is not elegant
    }
  }
};
</script>
