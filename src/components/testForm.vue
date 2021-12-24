<template>
  <form @submit="sendForm">
    <h2>Meu formulário</h2>
    <!-- <inputText type="text" v-model="name" /><br />
    <inputText type="email" v-model="email" /><br /> -->
    <input type="text" v-model='name'><br>
    <input type="text" v-model="email"><br>
    <submit />
  </form>
</template>

<script>
import inputText from "./form/inpuText.vue";
import submit from "./form/submit.vue";

export default {
  name: "testForm",
  components: {
    inputText,
    submit,
  },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    sendForm(e) {
      e.preventDefault();
      console.log("formulário enviado!");
      const name = this.name;
      const email = this.email;

      console.log(name)
      console.log(email)
    },
  },
};
</script>