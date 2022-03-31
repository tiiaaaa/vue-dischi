<template>
        <a href="#" class="album-card text-decoration-none text-muted p-3">
            <div class="card-immage mb-2">
                <img class="img-fluid rounded-circle" :src="album.poster" :alt="album.genre">
            </div>
            <div class="card-description text-center">
                <h3 class="fw-bold text-white mb-2">{{album.title}}</h3>
                <p class="mb-0">{{album.author}}</p>
                <span>{{album.year}}</span>
            </div>
        </a>
</template>

<script>
export default {
    name:'MainCard',
    props: {'album' : Object}

}
</script>

<style lang='scss' scoped>
    a.album-card{
        display: inline-block;
        width: calc(100% / 5);
        background-color: rgb(16, 14, 12);

        span{
            font-size: .9rem;
        }
    }

</style>