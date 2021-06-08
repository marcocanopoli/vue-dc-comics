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
            height: 190px;
            width: 100%;
            margin-bottom: 10px;  

            img {
                height: 100%;
                width: 100%;
                object-fit: cover;
                object-position: top;
            }
        }

        p {
            color: $textColor;
            text-transform: uppercase;
        }
    }

</style>