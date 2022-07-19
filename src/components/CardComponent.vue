<template>
  <div class="card-size p-3">
    <img src="disc.poster" alt="">
    <div class="text-center">
        <h2>{{ disc.author}}</h2>
        <p>foza jucve</p>
        <p>aaaaa</p>
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
    height: 130px;
}
.card-size{
    height: 300px;
    display: flex;
    flex-direction: column;
}
</style>