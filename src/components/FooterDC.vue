<template>
    <footer>
        <section>
            <div>

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
            </div>

            <div>
                <h3>DC</h3>
                <ul>
                    <li v-for="(element, i) in DC " :key="i">
                        <a href="#">{{ element }}</a>
                    </li>
                </ul>
            </div>

            <div>
                <h3>SITES</h3>
                    <ul>
                        <li v-for="(element, i) in sites " :key="i">
                            <a href="#">{{ element }}</a>
                        </li>
                    </ul>
            </div>
            <img src="../assets/img/dc-logo-bg.png" alt="logo DC">
        </section>

        <nav>

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
            sites: ["DC", "MAD Megazine", "DC Kids", "DC Universe", "DC Power Visa"]
        }
    }


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@mixin my-flex {
    display: flex;
    flex-direction: row;
}

section {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: contain;
    height: 300px;
    @include my-flex;
    justify-content: space-between;

    h3 {
        color: white;
    }

    ul {
        list-style-type: none;
        margin: 20px 0;

        li {

            a {
                text-decoration: none;
                color: grey;
                font-weight: bold;
                font-size: 15px;
            }
        }
    }
}

nav {}
</style>
