<template>
  <div class="card-size p-3">
    <div>
        <img :src="filtered.poster" alt="">
    </div>
    
    <div class="text-center pt-2">
        <h4>{{filtered.title}}</h4>
        <span class="pt-1 text-class">{{filtered.author}}</span>
        <p class="text-class">{{filtered.year}}</p>
    </div>
  </div>
</template>

<script>
export default {
    props:['filtered'],
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