<template>
  <li class="edu">
    <dt class="title">
      <q-icon name="school" size="sm"></q-icon>
      {{ $t(`title.education`) }}
    </dt>
    <ul class="content">
      <!-- TODO: v-for list perform-->
      <li>
        <span class="date">Sept 2019 - {{ $t(`present`) }}</span>
        <span class="details"
          ><span class="text-bold">{{ $t(`profile.degree`) }}</span
          >, {{ $t(`profile.uni`) }} <q-icon name="account_balance"></q-icon
        ></span>
      </li>
      <li>
        <span class="date">Sept 2016</span>
        <span class="details"
          ><span class="text-bold">{{ $t(`profile.high`) }}</span
          >, {{ $t(`profile.highSchool`) }}</span
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

<style scoped></style>
