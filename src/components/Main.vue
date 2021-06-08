<template>
  <main>
      <div>
        <Card   v-for="(comic, index) in comics" :key="index"
                :img-url="comic.thumb"
                :text="comic.series"/>
      </div>
  </main>
</template>

<script>
import Card from './Card.vue'
import series from '../data/series.js'

export default {
    name: 'Main',
    components: {
        Card
    },
    data() {
        return {
            comics: series
        }
    }
}
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";
    @import "../style/mixins.scss";

    main {        
        background-color: $secondColor;
        min-height: calc(100vh - 750px);

        & > div {
            @include container-center;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            padding-top: 50px;
        }
    }
</style>