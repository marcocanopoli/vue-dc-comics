<template>
    <header>
        <div>
            <img src="../assets/img/dc-logo.png" alt="DC logo">
            <ul>
                <li v-for="link, index in headerLinks" :key="index">
                    <a href="link.url" :class="{'active' : link.active}">{{ link.text }}</a>
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
            headerLinks: [
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
        display: flex;
        justify-content: space-between;        
        align-items: center;
        height: 120px;

        div {
            @include container-center;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;

            img {
                height: 70%;
            }

            ul {
                display: flex;
                height: 100%;
                list-style: none;

                a {                        
                    display: flex;
                    align-items: center;
                    height: 100%;
                    padding: 0 15px;
                    font-size: 14px;
                    color: $secondColor;
                    text-decoration: none;
                    text-transform: uppercase;
                    border-bottom: 5px solid transparent;

                    &.active,
                    &:hover {
                        border-bottom: 5px solid $mainColor;
                    }
                }
            }
        }
    }
</style>