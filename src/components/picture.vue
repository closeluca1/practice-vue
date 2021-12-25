<template>
    <img :src="avatar" :alt="description">
    <changeImg @changeImg="imgChange"/>
</template>

<script>
    import changeImg from './changeImg.vue';
    export default {
        name: 'pictureA',
        components: {
            changeImg
        },
        data() {
            return {
                avatar: 'https://conteudo.imguol.com.br/c/entretenimento/85/2021/07/16/alpaca-1626455789996_v2_4x3.jpg',
                description: 'ícone do Vue'
            }
        },
        methods: {
            imgChange() {
                console.log('imagem trocada');
                this.avatar = 'https://www.petz.com.br/blog/wp-content/uploads/2021/11/enxoval-para-gato-Copia.jpg'
            }
        }
    }
</script>

<style global>
img{
    width: 320px;
}

</style>