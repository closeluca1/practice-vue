<template>
    <div>
        <h1>Olá Vue!</h1>
        <reuse/>
        <reuse/>
        <reuse/>
        <reuse/>
        <reuse/>
        <p>Meu nome é {{ name }} e trabalho como {{ job }}.</p>
        <multipleEvents/>
        <reuse/>
    </div>
</template>

<script>
    import multipleEvents from './multipleEvents.vue';
    import reuse from './reuse.vue';
export default {
    name: 'firstComponent',
    components: {
        multipleEvents,
        reuse
    },
    data() {
        return {
            name: 'Patrick',
            job: 'Programador'
        }
    }
}
</script>