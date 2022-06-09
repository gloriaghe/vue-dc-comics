<template>
    <section>
        <div id="containerBuy">

            <div v-for="(element, i) in buy" :key="i">
                <a :href="element.link">
                    <img :src="element.img" :alt="element.name">
                    <span>{{ element.name }}</span>
                </a>

            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'SectionLink',
    data() {
        return {
            buy: [
                {
                    img: require("../assets/img/buy-comics-digital-comics.png"),
                    name: "DIGITAL COMICS",
                    link: "#"
                },
                {
                    img: require("../assets/img/buy-comics-merchandise.png"),
                    name: "DC MERCHANDISE",
                    link: "#"
                },
                {
                    img: require("../assets/img/buy-comics-shop-locator.png"),
                    name: "SUBSCRIPTION",
                    link: "#"
                },
                {
                    img: require("../assets/img/buy-comics-subscriptions.png"),
                    name: "COMIC SHOP LOCATOR",
                    link: "#"
                },
                {
                    img: require("../assets/img/buy-dc-power-visa.svg"),
                    name: "DC POWER VISA",
                    link: "#"
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
};

section {
    background-color: #0282f9;
    @include my-flex;
    justify-content: center;

    #containerBuy {
        width: 75%;
        @include my-flex;
        justify-content: space-between;
        flex-wrap: wrap;

        div {
            width: 20%;
            @include my-flex;
            justify-content: center;

            a {
                color: white;
                text-decoration: none;
                margin: 40px 0;
                @include my-flex;
                align-items: center;
                font-size: 15px;

                img {
                    width: 80px;
                    padding: 0 15px;
                }
            }

            @media screen and (max-width: $small ) {
                & {
                    width: 30%;
                }
            }
        }



    }
}
</style>
