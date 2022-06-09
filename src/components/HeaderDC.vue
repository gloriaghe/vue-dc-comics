<template>
    <header>
        <section>

            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="Logo Dc Comics">
            </a>
            <nav>
                <ul>
                    <li v-for="(link, i) in links" :key="i">
                        <a :href="link.url" :class="link.current ? 'here' : ''">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
            </nav>
        </section>
    </header>
</template>

<script>
export default {
    name: 'HeaderDC',
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                }
            ]
        }
    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
//media query
$medium: 1200px;

@mixin my-flex {
    display: flex;
    flex-direction: row;
}

;

header {

    @include my-flex;
    justify-content: space-around;
    align-items: center;
    height: 130px;

    section {
        @include my-flex;
        justify-content: space-between;
        width: 75%;

        img {
            width: 80px;
        }

        ul {
            list-style-type: none;
            margin: 20px 0;

            li {
                display: inline-block;
                padding: 10px;

                a {
                    text-decoration: none;
                    color: black;
                    font-weight: bold;
                    font-size: 15px;


                    &.here {
                        border-bottom: 4px solid #53b0f0;
                        padding-bottom: 55px;
                        color: #53b0f0;
                    }

                    @media screen and (max-width: $medium ) {
                        &.here {
                            padding-bottom: 15px;

                        }
                    }

                    &:hover {
                        color: #53b0f0;
                    }
                }
            }
        }
    }


}
</style>
