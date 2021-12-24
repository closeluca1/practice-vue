<template>
    <h1>Meu nome é: {{ name }}.</h1>
</template>

<script>
    export default {
        name: 'lifeCycle',
        data() {
            return {
                name: 'Ainda não sei'
            }
        },
        created() {
            setTimeout(() => {
                this.name = 'Patrick'
            }, 1000);
            this.lifeCicle()
        },
        mounted() {
            setTimeout(() => {
                this.name = 'Luca'
            }, 2000);
        },
        methods: {
            lifeCicle() {
                console.log('executado')
            }
        }
    }
</script>