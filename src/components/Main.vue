<template>
  <main>
      <div>
        <h1>My Content</h1>
      </div>
  </main>
</template>

<script>
export default {
    name: 'Main'
}
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";
    @import "../style/mixins.scss";

    main {
        background-color: $secondColor;
        height: 120px;
        div {
            @include container-center;
            h1 {
                text-align: center;
                color: #fff;
            }
        }
    }
</style>