<template>
  <div class="card-size p-3">
    <img :src="disc.poster" alt="">
    <div class="text-center pt-4">
        <h4>{{disc.title}}</h4>
        <span class="pt-1 text-class">{{disc.author}}</span>
        <p class="text-class">{{disc.year}}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:['disc'],
}
</script>

<style lang="scss" scoped>
img{
    height: 187px;
    widows: 187px;
}
.card-size{
    height: 350px;
    display: flex;
    flex-direction: column;
}
.text-class{
    font-size: 0.85rem;
    color: grey
}
</style>