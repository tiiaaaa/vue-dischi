<template>
    <main>
        <MainAlbumCard/>

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
            })
            .catch((error) => {
                console.log(error)
            })
        }
    }

}
</script>

<style lang='scss' scoped>

</style>