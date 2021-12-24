<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ test }}</h2>
        <info :email='email' :on_job='true'/>
        <testForm/>
    </div>
</template>

<script>
    import info from './info.vue';
    import testForm from './testForm.vue';
    export default {
        name: 'people',
        components: {
            info,
            testForm
        },
        data() {
            return {
                test: 'Patrick',
                email: 'jhon@email.com'
            }
        }
    }
</script>