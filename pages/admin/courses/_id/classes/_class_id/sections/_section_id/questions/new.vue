<template>
  <v-layout justify-center>
    <v-flex ref="flex" xs10 sm8 md4>
      <h1>Adicionar questão</h1>
      Seção: <n-link to="../edit">{{section.title}}</n-link>
      <v-form>
        <v-textarea
          label="Enunciado"
          required
        />
        <v-select
          :items="items"
          item-value="id"
          item-text="letter"
          label="Alternativa correta"
        />
        <v-textarea v-for="item in items" v-bind:key="item.id"
          :label="`Alternativa ${item.letter}`"
          required
        />
        <v-btn color="primary">Criar</v-btn>
      </v-form>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
    computed: {
        section() {
            return this.$store.state.courses.currentSection
        }
    },
    data: () => ({
      items: [
        { letter: 'A', id: 0 },
        { letter: 'B', id: 1 },
        { letter: 'C', id: 2 },
        { letter: 'D', id: 3 },
      ]
    })
}
</script>
