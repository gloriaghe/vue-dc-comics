<template>
    <section>
        <div v-for="(element, i) in buy" :key="i">
            <a :href="element.link">
                <img :src="element.img" :alt="element.name">
                <span>{{element.name}}</span>
            </a>

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
                    img: "../assets/img/buy-comics-digital-comics.png",
                    name: "DIGITAL COMICS",
                    link: "#"
                },
                {
                    img: "../assets/img/buy-comics-digital-merchandise.png",
                    name: "DC MERCHANDISE",
                    link: "#"
                },
                {
                    img: "../assets/img/buy-comics-shop-locator.png",
                    name: "SUBSCRIPTION",
                    link: "#"
                },
                {
                    img: "../assets/img/buy-comics-subscriptions.png",
                    name: "COMIC SHOP LOCATOR",
                    link: "#"
                },
                {
                    img: "../assets/img/buy-dc-power-visa.svg",
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
section {
    background-color: #0282f9;
}
</style>
