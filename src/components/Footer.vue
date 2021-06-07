<template>
    <footer>
        <div class="top">
            <!-- first col -->
            <div>
                <h2>DC Comics</h2>
                <ul>
                    <li>
                        <a href="#">Characters</a>
                    </li>
                    <li>
                        <a href="#">Comics</a>
                    </li>
                    <li>
                        <a href="#">Movies</a>
                    </li>
                    <li>
                        <a href="#">TV</a>
                    </li>
                    <li>
                        <a href="#">Games</a>
                    </li>
                    <li>
                        <a href="#">Videos</a>
                    </li>
                    <li>
                        <a href="#">News</a>
                    </li>
                </ul>

                <h2>Shop</h2>
                <ul>
                    <li>
                        <a href="#">Shop DC</a>
                    </li>
                    <li>
                        <a href="#">Shop DC Collectibles</a>
                    </li>
                </ul>
            </div>
            <!-- /first col -->

            <!-- second col -->
            <div>
                <h2>DC</h2>
                <ul>
                    <li>
                        <a href="#">Terms of Use</a>
                    </li>
                    <li>
                        <a href="#">Privacy Policy</a>
                    </li>
                    <li>
                        <a href="#">Ad choices</a>
                    </li>
                    <li>
                        <a href="#">Advertising</a>
                    </li>
                    <li>
                        <a href="#">Jobs</a>
                    </li>
                    <li>
                        <a href="#">Subscriptions</a>
                    </li>
                    <li>
                        <a href="#">Talent Workshops</a>
                    </li>
                    <li>
                        <a href="#">CPSC Certificates</a>
                    </li>
                    <li>
                        <a href="#">Ratings</a>
                    </li>
                    <li>
                        <a href="#">Shop Help</a>
                    </li>
                    <li>
                        <a href="#">Contact Us</a>
                    </li>
                </ul>
            </div>    
            <!-- /second col -->

            <!-- third col -->
            <div>
                <h2>Sites</h2>
                <ul>
                    <li>
                        <a href="#">DC</a>
                    </li>
                    <li>
                        <a href="#">Mad Magazine</a>
                    </li>
                    <li>
                        <a href="#">DC Kids</a>
                    </li>
                    <li>
                        <a href="#">DC Universe</a>
                    </li>
                    <li>
                        <a href="#">DC Power Visa</a>
                    </li>
                </ul>
            </div>
            <!-- /third col -->
        </div>

        <div class="bottom-container">
            <div class="bottom">

            </div>
        </div>
    </footer>    
</template>

<script>
export default {
    name : 'Footer'
}
</script>

<style lang="scss" scoped>
    @import "../style/variables.scss";
    @import "../style/mixins.scss";

    footer {
        background: url("../assets/img/footer-bg.jpg") no-repeat top;
        background-size: cover
    }

    .top,
    .bottom {
        @include container-center;
    }

    h2 {
        padding: 10px 0;
        color: #fff;
        text-transform: uppercase;
    }

    ul {
        list-style: none;
    }

    .top {
        display: flex;
        height: 370px;
        padding: 30px 0;
        
        div {
            margin-right: 50px;

            a {
                display: inline-block;
                text-decoration: none;
                padding: 2px 0;
                color: scale-color(#fff, $lightness: -40%);
            }
        }
    }

    .bottom-container {
        height: 150px;
        background-color: scale-color($secondColor, $lightness: +10%);
    }
</style>