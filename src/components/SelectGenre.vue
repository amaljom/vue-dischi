<template>
    <div class="col-6 mx-auto">
        <select class="form-select" aria-label="Default select example" v-model="selected">
            <option disabled value="">scegli il genere</option> 
            <option>Pop</option>
            <option>Rock</option>
            <option>Metal</option>
            <option>Jazz</option>
        </select>
    </div> 
   
</template>

<script>
export default {
    data: function(){
            return{
                selected:'' 
            }
            
        },
}
</script>

<style scoped lang="scss">
    .aooo{
        height: 50px;
        background-color: white;
    }
</style>