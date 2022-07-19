<template>
    <div class="p-0 d-flex flex-wrap justify-content-between">
        <CardComponent class="bg-card my-2 text-white"
        v-for="(disc,index) in discs" :key='index'
        :disc=disc />
    </div>
</template>

<script>
    import axios from 'axios';
    import CardComponent from './CardComponent';

    export default {
        data: function(){
            return{
                discs:[]
            }
            
        },
        
        components:{
            CardComponent,
        },
        
        methods:{
            
            getCards(){
                axios.get('https://flynn.boolean.careers/exercises/api/array/music')
                .then((result)=>{
                    this.discs = result.data.response;
                    console.log(this.discs);
                });
            }   
        },
        created(){
            this.getCards();
        }
    }
</script>

<style lang="scss">

.bg-card{
    background-color:#2e3a46;
    width: calc(100% / 5 - 35px);
}

</style>