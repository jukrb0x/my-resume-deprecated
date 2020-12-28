<template>
  <q-page padding>
    <!-- content -->
    <div :class="mainCSS">
      <!-- quick facts -->
      <div class="quick-facts">
        <!-- left -->
        <div class="profilo">
          <div class="avatar">
            <img src="~assets/avatar.jpg" width="115px" alt="" />
          </div>
          <div class="lang-btn">
            <LangSelector
              :current-lang-code="currentLangCode"
              :switch-lang="switchLang"
            ></LangSelector>
          </div>
        </div>

        <!-- medium -->
        <div class="info">
          <div class="facts">
            <div class="name">{{ $t(`profile.name`) }}</div>
            <div class="motto">{{ $t(`profile.motto`) }}</div>
            <div class="dept">{{ $t(`profile.dept`) }}</div>
            <div class="uni">{{ $t(`profile.uni`) }}</div>
          </div>
          <div class="contact">
            <!-- phone number -->
            <q-chip
              class="scale-up"
              outline
              icon="phone"
              color="primary"
              text-color="white"
            >
              {{ contact.tel }}
              <q-tooltip :offset="[10, 10]">
                {{ $t(`profile.phone`) }}
              </q-tooltip>
            </q-chip>

            <!-- email -->
            <q-chip
              class="scale-up"
              outline
              icon="mail"
              color="deep-orange"
              text-color="white"
            >
              {{ contact.email }}
              <q-tooltip :offset="[10, 10]">
                {{ $t(`profile.email`) }}
              </q-tooltip>
            </q-chip>

            <!-- website -->
            <a href="https://wh0.is" target="_blank">
              <q-chip
                class="scale-up"
                outline
                icon="language"
                color="red"
                text-color="white"
              >
                {{ contact.website }}
                <q-tooltip :offset="[10, 10]">
                  {{ $t(`profile.website`) }}
                </q-tooltip>
              </q-chip>
            </a>

            <!-- github -->
            <a href="https://github.com/jukrb0x" target="_blank">
              <q-btn
                class="scale-up"
                flat
                round
                color="indigo"
                icon="fab fa-github"
              >
                <q-tooltip :offset="[10, 10]">
                  jukrb0x
                </q-tooltip>
              </q-btn>
            </a>
          </div>
        </div>
        <!-- right -->
        <!--        <div class="contact">-->
        <!--          <q-chip icon="phone">{{ contact.tel }}</q-chip>-->
        <!--          <q-chip icon="mail">{{ contact.email }}</q-chip>-->
        <!--          <q-chip icon="language">{{ contact.website }}</q-chip>-->
        <!--        </div>-->
      </div>

      <div class="context">
        <!-- Education -->
        <Education />
        <!-- Experience -->
        <Experience />
        <!-- Skills -->
        <Skills />
        <!-- Research -->
        <Research />
      </div>
    </div>
    <!-- bottom -->
    <!-- latest update timestamp-->
    <div class="latest">
      <Timestamp />
    </div>
  </q-page>
</template>

<script>
import LangSwitchMixin from '../components/mixins/LangSwitchMixin';
import ContactInfoMixin from '../components/mixins/ContactInfoMixin';
import Education from '../components/Education';
import Experience from '../components/Experience';
import Research from '../components/Research';
import Skills from '../components/Skills';
import Timestamp from '../components/Timestamp';
export default {
  mixins: [LangSwitchMixin, ContactInfoMixin],
  components: {
    Timestamp,
    Skills,
    Research,
    Experience,
    Education,
    LangSelector: () => import('../components/LangSelector.vue')
  },
  data() {
    return {};
  },
  mounted() {
    console.log(this.$i18n);
  },
  methods: {},

  computed: {
    mainCSS: function() {
      return this.currentLangCode === 'zh-cn' ? 'chinese-font main' : 'main';
    }
  }
};
</script>

<style lang="sass" scoped>
.main
  background: #fff
  padding: 25px
  width: 1060px
  box-shadow: 0 3px 18px 2px rgba(0, 0, 0, 0.14), 0 3px 1px -3px rgba(0, 0, 0, 0.2), 0 1px 5px 0 rgba(0, 0, 0, 0.12)

  .quick-facts
    display: grid
    grid-template-columns: 140px 1000px
    margin-bottom: 25px
    .info
      .facts
        font-family: Georgia, "Microsoft Sans Serif"
        .name
          font-size: xx-large

    .contact
      margin-top: 5px
      margin-left: -5px
.latest
  display: flex
  justify-content: center
  margin-top: 20px
</style>
