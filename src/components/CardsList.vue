<template>
    <div class="col-2 card-size bg-success p-3">
        <CardComponent/>
    </div>
</template>

<script>
import CardComponent from './CardComponent';
export default {
    components: {
        CardComponent
    }
}
</script>

<style>
.card-size{
    height: 300px;
    display: flex;
    justify-content: center;
}


</style>