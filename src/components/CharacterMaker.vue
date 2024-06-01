<template>
  <div>
    <h1>Character maker</h1>
    <div>
      <h3>Selecione o Sistema que deseja criar o personagem</h3>
      <select class="selector" name="sistema" id="sistema" v-model="character.sistema">
        <option value=""></option>
        <option v-for="item in sistemas" :value=item.value v-bind:key="item">{{item.name}}</option>
      </select>
      <h3>Dê uma breve descrição do personagem</h3>
      <textarea class="description" name="description" id="description" v-model="character.description"></textarea>
      <h3>Qual o nível de poder do personagem?</h3>
      <select class="selector" name="nivelPoder" id="nivelPoder" v-model="character.nivelPoder">
        <option value=""></option>
        <option v-for="(item, index) in nivelPoder" :key="index" :value=item.value>{{item.name}}</option>
      </select>
    </div>
    {{ character }}
  </div>
</template>

<script>
let selector
export default {
  name: 'CharacterMaker',
  data () {
    return {
      selector,
      sistemas: [{ name: 'Vampiro: a máscara 20 anos', value: 1 }, { name: 'Mago: a Ascensão 20 anos', value: 2 }, { name: 'Pathfinder 2e', value: 3 }, { name: 'Dungeon Crawl Classics', value: 4 }],
      nivelPoder: [{ name: 'Abaixo da party', value: 0 }, { name: 'Mesmo da party', value: 1 }, { name: 'Mais forte que a party', value: 2 }, { name: 'Boss Menor', value: 3 }, { name: 'BBEG', value: 4 }],
      character: {}
    }
  }
}
</script>

<style>
.selector {
  padding: 5px,
}

.description {
  width: 400px;
  height: 160px;
}

</style>
