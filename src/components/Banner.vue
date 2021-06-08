<template>
    <section>
        <div class="box">
            <div v-for="item, index in buyItems" :key="index">
                <img :src="item.imgPath" alt="">
                <span>{{ item.text }}</span>
            </div>
        </div>
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
                    imgPath : require('../assets/img/buy-comics-digital-comics.png')
                },
                {
                    text : 'DC Merchandise',
                    imgPath : require('../assets/img/buy-comics-merchandise.png')
                },
                {
                    text : 'Subscription',
                    imgPath : require('../assets/img/buy-comics-subscriptions.png')
                },
                {
                    text : 'Comic Shop Locator',
                    imgPath : require('../assets/img/buy-comics-shop-locator.png')
                },
                {
                    text : 'DC Power Visa',
                    imgPath : require('../assets/img/buy-dc-power-visa.svg')
                },
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

        .box {
            @include container-center;
            @include flex-center('vertical');
            height: 100%;

            div {
                @include flex-center('vertical');
                width: 100%;
                justify-content: space-evenly;

                img {
                    max-height: 60px;
                    max-width: 60px;
                }
    
                span {
                    display: block;
                    margin-left: 20px;
                    text-transform: uppercase;
                    color: $textColor;
                }
            }
        }
    }
</style>