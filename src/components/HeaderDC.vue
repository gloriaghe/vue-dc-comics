<template>
    <header>
        <a href="#">
            <img src="../assets/img/dc-logo.png" alt="Logo Dc Comics">
        </a>
        <nav>
            <ul>
                <li v-for="(link, i) in links" :key="i">
                    <a :href="link.url" >
                        {{link.text}}
                    </a>
                </li>
            </ul>
        </nav>
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
header{
    display: flex;
    flex-direction: row;
    justify-content: space-around;

    ul{
        list-style-type: none;
        margin: 20px 0;
        
        li{
            display: inline-block;
            padding: 10px;

            a{
                text-decoration: none;
                color: black;
                font-weight: bold;
            }
        }
    }

}

</style>
