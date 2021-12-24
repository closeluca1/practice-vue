<template>
  <div>
    <button @click="first(txt1, $event), second(txt2, $event)">
      ativar multiplos eventos
    </button>
    <p>{{ multiple_events }}</p>
  </div>
</template>


<script>
export default {
  name: "multipleEvents",
  data() {
    return {
      multiple_events: "",
      txt1: "primeiro evento",
      txt2: "segundo evento",
    };
  },
  methods: {
    first(txt1, e) {
      e.preventDefault();
      this.multiple_events = txt1;
    },
    second(txt2, e) {
      setTimeout(() => {
        this.multiple_events = txt2;
      }, 1000);
    },
  },
};
</script>

<style scoped>
div {
  margin: 100px;
}
</style>