<template>
    <div class="flex-wrap">
        <a href="#" class="album-card text-decoration-none text-muted p-2">
            <div class="card-immage">
                <img src="" alt="">
            </div>
            <div class="card-description"></div>
        </a>
    </div>
</template>

<script>
export default {
    name:'MainCard',

}
</script>

<style lang='scss' scoped>
    a.album-card{
        display: inline-block;
        width: calc(100% / 5);
        height: 300px;
        background-color: antiquewhite;
    }

</style>