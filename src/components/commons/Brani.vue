<template>
    <div class="box">
        <div class="cover">
            <img :src="informazioni.poster" 
            :alt="informazioni.name">
        </div>
        <div class="title">
            {{informazioni.title}}
        </div>
        <div class="info">
            <div class="author">
                {{informazioni.author}}
            </div>
            <div class="year">
                {{informazioni.year}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Brani',
    props: {
        informazioni: Object
    }
}
</script>

<style lang='scss' scoped>
    .box{
        height: 400px;
        width: calc((100% - 150px) / 5);
        background-color: #2e3a46;
        margin-bottom: 20px;

        img{
            height: 170px;
            width: 170px;
            margin: 20px auto;
        }

        .title{
            font-size: 25px;
            color: white;
            font-weight: bold;
            text-transform: uppercase;
        }

        .info{
            color: #8b8888;
            margin-top: 20px;
            font-size: 17px;
        }
    }
</style>