<template>
    <footer>
        <section id="sectionFooter">
            <div id="linkFooter">
                <section>

                    <div>
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(element, i) in dcComics " :key="i">
                                <a href="#">{{ element }}</a>
                            </li>
                        </ul>
                    </div>

                    <div>
                        <h3>SHOP</h3>
                        <ul>
                            <li v-for="(element, i) in shop " :key="i">
                                <a href="#">{{ element }}</a>
                            </li>
                        </ul>
                    </div>
                </section>

                <section>
                    <h3>DC</h3>
                    <ul>
                        <li v-for="(element, i) in DC " :key="i">
                            <a href="#">{{ element }}</a>
                        </li>
                    </ul>
                </section>

                <section>
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="(element, i) in sites " :key="i">
                            <a href="#">{{ element }}</a>
                        </li>
                    </ul>
                </section>

                <img id="logo" src="../assets/img/dc-logo-bg.png" alt="logo DC">
            </div>
        </section>

        <nav>
            <div>
                <button>
                    <a href="#">SIGN-UP NOW!</a>
                </button>
                <div id="social">
                    <a id="follow" href="#">FOLLOW US</a>
                    <div id="containersocialFooter">
                        <a href="#" v-for="(element, i) in footerSocial" :key="i">
                            <img :src="element.img" :alt="element.name">
                        </a>
                    </div>
                </div>
            </div>
        </nav>
    </footer>
</template>

<script>

export default {
    name: 'FooterDC',
    data() {
        return {
            dcComics: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"],
            shop: ["Shop DC", "Shop DC Collectibles"],
            DC: ["Terms of use", "Privacy Policy(New)", "Ad Choices", "Advertising", "Jobs", "Subscription", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
            sites: ["DC", "MAD Megazine", "DC Kids", "DC Universe", "DC Power Visa"],
            footerSocial: [
                {
                    img: require("../assets/img/footer-facebook.png"),
                    name: "Facebook"
                },
                {
                    img: require("../assets/img/footer-twitter.png"),
                    name: "Twitter"
                },
                {
                    img: require("../assets/img/footer-youtube.png"),
                    name: "YouTube"
                },
                {
                    img: require("../assets/img/footer-pinterest.png"),
                    name: "Pinterest"
                },
                {
                    img: require("../assets/img/footer-periscope.png"),
                    name: "Periscope"
                }
            ]
        }
    }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
//media query
$small: 1100px;

@mixin my-flex {
    display: flex;
    flex-direction: row;
}

#sectionFooter {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    @include my-flex;
    justify-content: space-evenly;

    #linkFooter {
        @include my-flex;
        justify-content: space-between;
        width: 75%;
        height: 350px;
        overflow: hidden;

        section {
            margin-top: 30px;

            h3 {
                color: white;
                text-align: start;
            }

            ul {

                list-style-type: none;
                margin: 20px 0;

                li {
                    text-align: start;

                    a {
                        text-decoration: none;
                        color: grey;
                        font-weight: bold;
                        font-size: 15px;
                    }
                }
            }
        }
    }

    #logo {
        width: 50%;
        object-fit: contain;
        margin-top: -40px;
        margin-bottom: -40px;

    }
}

nav {
    @include my-flex;
    justify-content: center;
    align-items: center;
    background-color: #303030;
    height: 130px;
    // z-index: 100;
    // position: fixed;
    // bottom: 0;
    // left: 0;
    width: 100%;

    div {
        @include my-flex;
        justify-content: space-between;
        width: 75%;

        button {
            background-color: #303030;
            border: 2px solid #0282f9;
            padding: 15px;
        }

        a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: 15px;
        }

        #social {
            width: 35%;
            @include my-flex;
            align-items: center;

            #follow {
                color: #0282f9;
                font-size: 20px;
                font-weight: bold;
            }

            @media screen and (max-width: $small ) {
                & {
                    width: 50%;

                }
            }
        }
    }
}
</style>
