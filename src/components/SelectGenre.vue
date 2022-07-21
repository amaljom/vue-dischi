<template>
    <div>
        <div class="col-6 mx-auto">
        <select class="form-select" aria-label="Default select example" v-model="Selected" @change="$emit('search',Selected )"> 
            <option value="">mostra tutti</option>
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
    
</style>