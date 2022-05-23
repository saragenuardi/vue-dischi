<template>

  <main  class="py-4">
      <div class="container">
          <div class="m-5 row row-cols-5">
              <AppCard v-for="(album, index) in albums" :key="index" :album="album" />
          </div>
      </div>

  </main>

</template>

<script>
import AppCard from './AppCard.vue';
import axios from 'axios';
export default {
    components: {
        AppCard
    },
    name: "AppMain",
    data() {
        return {
            albums: [],
        }
    },
    created()  {
        axios
        .get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((resp) => {
            this.albums = resp.data.response;
            console.log(resp)
        }
        )
    }
};
</script>

<style scoped lang="scss">
    main {
        background-color: #1E2D3B;
    }
</style>