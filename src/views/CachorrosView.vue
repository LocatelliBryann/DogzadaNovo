<script>
import CachorroCard from "@/components/cachorrada/CachorroCard.vue";
import axios from "axios";
export default {
  components: { CachorroCard },
  data() {
    return {
      cachorros: [],
    };
  },
  async created() {
    const cachorros = await axios.get("http://191.52.55.180:8000/cachorros/");
    this.cachorros = cachorros.data;
  },
};
</script>
<template>
  <div class="card-group">
    <CachorroCard
      v-for="cachorro in cachorros"
      :key="cachorro.id"
      :cachorro="cachorro"
    />
  </div>
</template>

<style></style>
