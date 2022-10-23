<template>
  <div class="card">
        <a :href="item.href" target="_blank">
            <img :src="item.img" alt="Imagem do servico" />
        </a>
        <span>{{ item.titulo}}</span>
    </div>
</template>

<script>
export default {
    props:['item']
}
</script>

<style scoped>
    div{
        margin: 20px 50px 20px 50px;
        display: block;
        width: 100px;
    }
    img{
        width: 80px;
    }
    span{
        font-weight: 900;
    }
    .card{
        display: flex;
        justify-content: center;
        flex-direction: column;
        border: 1px solid gray;
        border-radius: 5%;
        min-width: 120px;
        min-height: 150px;
        box-shadow: 0 0 2em gray;
        opacity: .9;
        transition: box-shadow .5;
       
    }
    .card:hover{
        box-shadow: 0 0 4em gray;
        opacity: 1;

    }

</style>