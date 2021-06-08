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
                <a href="#" class="button">Sign-up now!</a>
                <div >
                    <span>Follow Us</span>
                    <ul>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-facebook.png" alt="facebook logo">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-twitter.png" alt="twitter logo">                                
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-youtube.png" alt="youtube logo">
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-pinterest.png" alt="pinterest logo">                                
                            </a>
                        </li>
                        <li>
                            <a href="#">
                                <img src="../assets/img/footer-periscope.png" alt="periscope logo">                                
                            </a>
                        </li>
                    </ul>
                </div>
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
        background-size: cover;
    }

    h2 {
        padding: 10px 0;
        color: $textColor;
        text-transform: uppercase;
    }

    .top,
    .bottom {
        @include container-center;
    }

    .top {
        display: flex;
        height: 370px;
        padding: 30px 0;
        background: url("../assets/img/dc-logo-bg.png") no-repeat;
        background-position: right center;
        
        div {
            margin-right: 30px;

            ul {
                list-style: none;
                a {
                    display: inline-block;
                    padding: 2px 0;
                    font-family: $altFont, sans-serif;
                    font-size: 12px;
                    text-decoration: none;
                    color: scale-color($textColor, $lightness: -40%);

                    &:hover {
                        color: $mainColor;
                    }
                }
            }
            
        }
    }

    .bottom-container {
        height: 120px;
        background-color: scale-color($secondColor, $lightness: +10%);

        .bottom {
            @include flex-center ('vertical');
            justify-content: space-between;
            height: 100%;

            .button {
                display: inline-block;
                padding: 15px;
                font-family: $altFont, sans-serif;
                font-size: 18px;
                font-weight: 700;
                text-transform: uppercase;
                text-decoration: none;
                border: 2px solid $mainColor;
                color: $textColor;
            }
            
            div {
                @include flex-center ('vertical');

                span {
                    margin-right: 30px;
                    font-size: 22px;
                    font-weight: 700;
                    text-transform: uppercase;
                    color: $mainColor;
                }

                ul {
                    @include inline-list;

                    li {
                        padding: 0 10px;
                    }
                }                              
            }
        }
    }
</style>