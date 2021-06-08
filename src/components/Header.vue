<template>
    <header>
        <div class="container">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="DC logo">
            </a>
            <ul>
                <li v-for="(item, index) in menu" :key="index">
                    <a href="link.url" :class="{'active' : item.active}">{{ item.text }}</a>
                </li>
            </ul>
        </div>        
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function() {
        return {
            menu: [
                {
                    text : 'Characters',
                    url : '#characters',
                    active : false
                },
                {
                    text : 'Comics',
                    url : '#comics',
                    active : true
                },
                {
                    text : 'Movies',
                    url : '#movies',
                    active : false
                },
                {
                    text : 'TV',
                    url : '#tv',
                    active : false
                },
                {
                    text : 'Games',
                    url : '#games',
                    active : false
                },
                {
                    text : 'Collectibles',
                    url : '#collectibles',
                    active : false
                },
                {
                    text : 'Videos',
                    url : '#videos',
                    active : false
                },
                {
                    text : 'Fans',
                    url : '#fans',
                    active : false
                },
                {
                    text : 'News',
                    url : '#news',
                    active : false
                },
                {
                    text : 'Shop',
                    url : '#shop',
                    active : false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";
    @import "../style/mixins.scss";

    header {
        @include flex-center ('vertical');
        justify-content: space-between;        
        height: 120px;

        div {
            @include container-center;
            @include flex-center ('vertical');
            justify-content: space-between;
            height: 100%;

            & > a {
                height: 70%;
            }

            & > a > img {
                height: 100%;
            }

            ul {
                @include inline-list;
                height: 100%;

                li {
                    padding: 0 15px;

                    a {                        
                        @include flex-center ('vertical');
                        position: relative;
                        height: 100%;
                        font-weight: 700;
                        text-decoration: none;
                        text-transform: uppercase;
                        color: scale-color($secondColor, $lightness: +20%);

                        &:hover,
                        &.active {
                            color: $mainColor;
                        }
                        &.active::after,
                        &:hover::after {
                            position: absolute;
                            content: '';
                            bottom: 0;
                            height: 5px;
                            width: 100%;
                            background-color: $mainColor;
                        }
                    }
                }
                
            }
        }
    }
</style>