<template>
  <li class="exp">
    <dt class="title">
      <q-icon name="explore" size="sm"></q-icon>
      {{ $t(`title.experience`) }}
    </dt>
    <ul class="content dated">
      <li>
        <span class="date">{{ $t(`graphery.date`) }}</span>
        <span class="details">
          <b>{{ $t(`graphery.job`) }}</b
          >, {{ $t(`graphery.title`) }}<br />{{ $t(`graphery.description`) }}
        </span>
      </li>
      <li>
        <span class="date">{{ $t(`vac.date`) }}</span>
        <span class="details">
          <b>{{ $t(`vac.job`) }}</b>, {{ $t(`vac.title`) }}<br />{{
            $t(`vac.description`)
          }}
        </span>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'Experience'
};
</script>

<style scoped></style>
