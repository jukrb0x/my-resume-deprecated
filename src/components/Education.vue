<template>
  <li class="edu">
    <dt class="title">
      <q-icon name="school" size="sm"></q-icon>
      {{ $t(`title.education`) }}
    </dt>
    <ul class="content dated">
      <!-- TODO: v-for list perform-->
      <li>
        <span class="date">Sept 2019 - {{ $t(`present`) }}</span>
        <span class="details"
          ><span class="text-bold">{{ $t(`profile.degree`) }}</span
          >,
          <a class="uni-link" href="http://www.xmu.edu.my/" target="_blank"
            >{{ $t(`profile.uni`) }} <q-icon name="account_balance"></q-icon
          ></a>
        </span>
      </li>
      <li>
        <span class="date">{{ $t(`profile.highSchool.date`) }}</span>
        <span class="details"
          ><span class="text-bold">{{ $t(`profile.highSchool.degree`) }}</span
          >, {{ $t(`profile.highSchool.schoolName`) }}</span
        >
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'Education'
};
</script>

<style lang="sass" scoped>
a
  color: black
a
  transition: .3s ease

a:hover
  color: $blue-10
</style>
