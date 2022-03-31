<template>
    <main>
        <div class="my-container">
            
            <MainAlbumCard/>
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
        // this.getApiLIst()
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
        height: 85vh;
        background-color: rgb(39, 39, 61);

        div.my-container{
            height: 100%;
            width: 80%;
            margin: 0 auto;
            padding: 3rem 0;
            background-color: aquamarine;
        }
    }

</style>