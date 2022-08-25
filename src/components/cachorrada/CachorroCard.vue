<script>
export default {
  props: ["cachorro"],
};
</script>

<template>
  <div class="card">
    <img
      src="@/assets/img/guia_racas_golden_retriever_dogvibe.jpg"
      alt="gato"
    />
    <h1>{{ cachorro.nome }}</h1>
    <div class="descricao">
    
      {{ cachorro.descricao }}
    </div>

    <div class="button">
      <button>clique aqui</button>
      <div class="help-link">
        <span><a href="#">Estou em apuros? Clique aqui</a></span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.descricao{
  display: flex;
  flex-wrap: wrap;
  width: 100%
}
</style>
