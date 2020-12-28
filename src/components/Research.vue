<template>
  <li class="rsch">
    <dt class="title">
      <q-icon name="science" size="sm"></q-icon>
      {{ $t(`title.research`) }}
    </dt>
    <ul class="content">
      <li>
        <span class="proj-name text-bold"
          >{{ $t(`proj.my-resume.title`)
          }}<a href="https://github.com/jukrb0x/my-resume" target="_blank">
            <q-btn flat round color="black" icon="fab fa-github" size="sm">
              <q-tooltip :offset="[10, 10]">
                {{ $t(`ghrepo`) }}
              </q-tooltip>
            </q-btn>
          </a>
        </span>
        <span class="description">{{ $t(`proj.my-resume.description`) }}</span>
      </li>
      <li>
        <span class="proj-name text-bold"
          >{{ $t(`proj.daka.title`)
          }}<a href="https://github.com/jukrb0x/Daka" target="_blank">
            <q-btn flat round color="black" icon="fab fa-github" size="sm">
              <q-tooltip :offset="[10, 10]">
                {{ $t(`ghrepo`) }}
              </q-tooltip>
            </q-btn>
          </a>
        </span>
        <span class="description">{{ $t(`proj.daka.description`) }}</span>
      </li>
      <li>
        <span class="proj-name text-bold"
          >{{ $t(`proj.graphery.title`)
          }}<a href="https://github.com/FlickerSoul/Graphery/" target="_blank">
            <q-btn flat round color="black" icon="fab fa-github" size="sm">
              <q-tooltip :offset="[10, 10]">
                {{ $t(`ghrepo`) }}
              </q-tooltip>
            </q-btn>
          </a>
        </span>
        <span class="description" style="white-space: pre"
          >{{ $t(`proj.graphery.description`)
          }}<a href="https://github.com/FlickerSoul/" target="_blank">
            <q-btn flat round color="black" icon="fas fa-user-circle" size="sm">
              <q-tooltip :offset="[10, 10]">
                {{ $t(`ghrepo`) }}
              </q-tooltip>
            </q-btn>
          </a>
        </span>
      </li>
      <li>
        <span class="proj-name text-bold">{{ $t(`exploring`) }}</span>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'Research'
};
</script>

<style lang="sass" scoped>
ul.content > li
  display: grid
  grid-template-rows: auto auto
</style>
