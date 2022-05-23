<template>
  <div>
    <imput type="text" placeholder="Cerca canzone" v-model="ricerca">
      <button @click="$emit('searchClick', ricerca)">Cerca</button>
    </imput>
  </div>
</template>


<script>
export default {
  name: "AppSearch",
  data: function () {
    return {
      ricerca: "",
    };
  },
};
</script>

<style>
</style>