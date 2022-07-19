<template>
    <div class="p-0">
        <CardComponent class="col-2  bg-success"
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

<style>



</style>