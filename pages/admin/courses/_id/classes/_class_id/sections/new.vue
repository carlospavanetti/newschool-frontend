<template>
  <v-layout justify-center>
    <v-flex ref="flex" xs10 sm8 md4>
      <h1>Adicionar seção de aula</h1>
      Aula: <n-link to="../edit">{{klass.title}}</n-link>
      <v-form>
        <v-text-field
          label="Título"
          required
        />
        <v-textarea
          label="Descrição"
          required
        />
        <v-text-field
          label="Link para o youtube"
          required
        />
        <v-text-field
          label="Link para o vimeo"
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
        klass() {
            return this.$store.state.courses.currentClass
        }
    }
}
</script>
