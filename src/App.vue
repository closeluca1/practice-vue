<template>
  <div>
    <h1>ola mundo!</h1>
    <firstComponent />
    <p>O dado de #App é {{ test }}</p>
    <lifeCycle />
    <people />
  </div>
</template>

<script>
import firstComponent from "./components/firstComponent.vue";
import lifeCycle from "./components/lifeCycle.vue";
import people from "./components/peoples.vue";

export default {
  components: {
    firstComponent,
    lifeCycle,
    people,
  },
  data() {
    return {
      test: "Testando",
    };
  },
};
</script>

<style>
body {
  color: #fafafa;
  background: #1a1a1a;
}
a {
  color: red;
}
</style>