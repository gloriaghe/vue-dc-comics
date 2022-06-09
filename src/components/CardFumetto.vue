<template>
   <div>
       <img :src="img" :alt="text">
       <span>{{text}}</span>
   </div>
</template>

<script>

export default {
    name: 'CardFumetto',
    props: {
        img: String,
        text: String
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
//media query
$medium: 1400px;
$small: 1000px;

div{
    flex-basis: 15%;
    padding: 30px 0;

    img{
        width: 80%;
        max-height: 180px;
        object-fit: cover;
        object-position: top;

    }

    span {
        display: block;
        width: 80%;
        text-align: start;
        text-transform: uppercase;
        margin-top: 15px;
        margin-left: 25px;
        font-size: 15px;
    }

}

@media screen and (max-width: $medium ){
    div{
        flex-basis: 20%;
    }
}
@media screen and (max-width: $small ){
    div{
        flex-basis: 25%;
    }
}
</style>
