<template>
  <div class="main-background">
    <div class="row col-8 mx-auto pt-5">
        <CardsList/>
    </div>
  </div>
</template>

<script>
import CardsList from './CardsList';
export default {
    components: {
        CardsList
    },
}


</script>

<style>
.main-background{
    height: calc( 100vh);
    background-color: #1E2D3B;
}
</style>