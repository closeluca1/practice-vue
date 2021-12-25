<template>
    <div>
        <button @click="$emit('changeImg')">trocar imagem do perfil</button>
    </div>
</template>

<script>
    export default {
        name: 'changeImg',
        emits: ['changeImg']
    }
</script>