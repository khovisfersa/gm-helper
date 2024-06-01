<template>
  <div class="home">
    <CharacterMaker />
  </div>
</template>

<script>
// @ is an alias to /src
import CharacterMaker from '@/components/CharacterMaker.vue'

export default {
  name: 'HomeView',
  components: {
    CharacterMaker
  }
}
</script>
