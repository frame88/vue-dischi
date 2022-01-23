<template>
    <main>
        <Search
            @emitSearch="getOption($event)"
         />
        <div class="container p-5">
            <div v-if="cards" class="row row-cols-5 cards g-3">
                <Card
                v-for="(card, index) in cards"
                :key="index"
                :card="card"
                />
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios';
import Card from './Card.vue';
import Search from './Search.vue';
export default {
    name: 'Main',
    components: {
        Card,
        Search,
    },
    data (){
        return{
            cards : null,
            option: null,
            queryApi: "https://flynn.boolean.careers/exercises/api/array/music",
        };
    },
    created(){
        this.getAxios()
    },
    methods: {
        getAxios: function(){
            axios.get(this.queryApi)
            .then((result) =>{
                this.cards = result.data.response;
                this.option = result.data.response;
            })
            .catch((error) =>{
                console.log(error);
            })
        },
        getOption: function(text){
            this.cards = this.option;
            if (text !="all"){
                let newArray = this.cards.filter(element =>{
                    if (element.genre.toLowerCase().includes(text.toLowerCase())){
                        return true;
                    }
                })
                this.cards = newArray;
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    main{
        background-color: #1E2D3B;
    }
    img{
        max-width: 100%;
    }
</style>