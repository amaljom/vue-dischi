<template>
    <div>
        <div v-if="discs.length>9" class="p-0 d-flex flex-wrap justify-content-between">
            <CardComponent class="bg-card my-2 text-white"
            v-for="(disc,index) in discs" :key='index'
            :disc=disc />
        </div>
        <div v-else>
            <div class="spinner"> </div>
        </div>
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
    width: calc(100% / 5 - 30px);
}
.spinner{
    height: 120px;
    width: 120px;
    margin: 0 auto;
    margin-top: 40px;
    border: solid 10px rgb(255, 255, 255);
    border-radius: 50%;
    border-bottom: 10px solid rgb(49, 35, 63);
    animation: spin 1s linear infinite;

    @keyframes spin {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
}  
}

</style>