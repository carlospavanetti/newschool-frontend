<template>
  <v-layout justify-center>
    <v-flex ref="flex" xs10 sm8 md4>
      <h1>Adicionar aula</h1>
      Curso: <n-link to="../edit">{{course.title}}</n-link>
      <v-form>
        <v-text-field
          label="Título"
          required
        />
        <v-textarea
          label="Descrição"
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
        course() {
            return this.$store.state.courses.current
        }
    }
}
</script>
