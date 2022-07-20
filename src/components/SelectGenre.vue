<template>
<div>
    <div class="aooo">
        {{ Selected }}
    </div>
    <div class="col-6 mx-auto">
        <select class="form-select" aria-label="Default select example" v-model="Selected" @click="$emit('search','Selected')">
            <option disabled value="">scegli il genere</option> 
            <option>Pop</option>
            <option>Rock</option>
            <option>Metal</option>
            <option>Jazz</option>
        </select>
        </div>
    </div>
   
</template>

<script>
export default {
    data: function(){
            return{
                Selected:'' 
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