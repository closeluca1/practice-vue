<template>
    <div>
        <button @click='toActive'> clique aqui</button>
        <span v-show='actived'>Ativado!</span>
    </div>
</template>

<script>
    export default {
        name: 'reuse',
        data() {
            return {
                actived: false,
            }
        },
        methods: {
            toActive(){
                this.actived = !this.actived;
            }
        }
    }
</script>