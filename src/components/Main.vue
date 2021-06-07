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
        min-height: calc(100vh - 750px);
        div {
            @include container-center;
            padding: 50px 0;

            h1 {
                color: #fff;
            }
        }
    }
</style>