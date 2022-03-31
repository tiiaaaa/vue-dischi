<template>
    <main>
        <div class="my-container">
            <div v-for="(element, index) in albumList" :key="index">
                <MainAlbumCard :album="element"/>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios';
import MainAlbumCard from './MainAlbumCard.vue';

export default {
    name:'MainAlbum',
    components:{
        MainAlbumCard,
    },

    data: function(){
        return{
            albumList: null
        }
    },

    created: function(){
        this.getApiLIst()
    },

    methods: {
        getApiLIst(){
            axios
            .get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                console.table(response.data.response);
                this.albumList = response.data.response;
            })
            .catch((error) => {
                console.log(error)
            })
        }
    }

}
</script>

<style lang='scss' scoped>
    main{
        background-color: rgb(39, 39, 61);

        div.my-container{
            width: 80%;
            margin: 0 auto;
            padding: 3rem 0;
            background-color: aquamarine;
        }
    }

</style>