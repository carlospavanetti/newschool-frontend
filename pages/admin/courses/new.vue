<template>
  <v-layout justify-center>
    <v-flex ref="flex" xs10 sm8 md4>
      <h1>Adicionar curso</h1>
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
          label="Professor"
          required
        />
        <v-textarea
          label="Biografia do professor"
          required
        />
        <v-btn color="primary">Criar</v-btn>
      </v-form>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
}
</script>
