<template>
    <img :src="avatar" :alt="description">
</template>

<script>
    export default {
        name: 'pictureA',
        data() {
            return {
                avatar: 'https://conteudo.imguol.com.br/c/entretenimento/85/2021/07/16/alpaca-1626455789996_v2_4x3.jpg',
                description: 'ícone do Vue'
            }
        }   
    }
</script>