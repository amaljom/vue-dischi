<template>
  <div class="card-size p-3">
    <div>
        <img :src="disc.poster" alt="">
    </div>
    
    <div class="text-center pt-2">
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
    width: 100%;
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