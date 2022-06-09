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
div{
    img{
        width: 190px;
        max-height: 180px;
         object-fit: cover;
         object-position: top;
    }

    span {
        display: block;
    }

}


</style>
