
<template>
  <header>
    <div class="search-bar">
      <AppSearch @searchClick="datoRicevuto($event)" />
    </div>
  </header>
</template>



<script>
import AppSearch from "./AppSearch.vue";
export default {
  name: "AppHeader",
  components: {
    AppSearch
  },

  data: function () {
    return {
        testoCercato: "",
    } 
   
},
computed: {
    albumFiltred() {
        const filtredArray = this.cards.filter((item) => {
            return item.cards.toLowerCase().includes(this.testoCercato)
        }
        )
        return filtredArray;
    }
},

methods: {
  datoRicevuto(testo) {
      this.testoCercato = testo.toLowerCase();
  }
}
}


</script>

<style scoped lang="scss">
header {
  height: 80px;
  background-color: #2e3a46;
}
</style>
