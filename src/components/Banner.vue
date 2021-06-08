<template>
    <section>
        <ul>
            <li v-for="item, index in buyItems" :key="index">
                <img :src="item.imgName" alt="">
                <span>{{ item.text }}</span>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    name : 'Banner',
    data: function() {
        return {
            buyItems : [
                {
                    text : 'Digital comics',
                    imgName : require('../assets/img/buy-comics-digital-comics.png')
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";
    @import "../style/mixins.scss";

    section {
        height: 140px;
        background-color: $mainColor;

        ul {
            @include inline-list;
        }
    }
</style>