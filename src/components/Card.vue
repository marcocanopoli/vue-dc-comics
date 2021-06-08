<template>
    <div class="card">
        <div class="img-box">
            <img :src="imgUrl" :alt="text + 'thumb'">
        </div>
        <p>{{ text }}</p>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        imgUrl: String,
        text: String
    }
}
</script>

<style lang="scss" scoped>

    @import "../style/variables.scss";

    .card {
        width: 190px;
        margin-bottom: 50px;  

        .img-box {
            position: relative;
            height: 190px;
            width: 100%;
            margin-bottom: 10px;
            cursor: pointer;          

            img {                
                height: 100%;
                width: 100%;
                object-fit: cover;
                object-position: top;

                
            }

            &::after {
                position: absolute;
                content: '';
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
                height: 100%;
                width: 100%;
                background-color: scale-color($mainColor, $alpha: -30%);
                transition: .2s;
                opacity: 0;               
            }

            &:hover::after {
                opacity: 1;      
            }
        }

        p {
            color: $textColor;
            text-transform: uppercase;
        }
    }

</style>