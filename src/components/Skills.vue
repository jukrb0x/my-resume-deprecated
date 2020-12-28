<template>
  <li class="ski">
    <dt class="title">
      <q-icon name="support" size="sm"></q-icon>
      {{ $t(`title.skills`) }}
    </dt>
    <ul class="content">
      <li>
        <b>{{ $t(`skills.englishCert`) }}:</b> {{ $t(`skills.ielts`) }}
      </li>
      <li>
        <b>{{ $t(`justfine`) }}:</b> {{ $t(`skills.programming`) }}
      </li>
      <li>
        <b>{{ $t(`interest`) }}:</b> {{ $t(`profile.interests`) }}
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'Skills'
};
</script>

<style scoped></style>
