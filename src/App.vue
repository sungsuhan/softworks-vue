<template>
  <div class="name">
    {{ name }}
  </div>
  <button class="btn btn-primary" v-on:click="updateName">
    Click
  </button>
</template>



<script>
import { reactive } from "vue";

export default {
  setup() {
    const name = reactive('softworks');

    const greeting = (name) => {
      return 'Hello, ' + name;
    };

    const greet = greeting(name);

    const updateName = () => {
      name.value = 'SW';
      console.log(name);
    };

    return {
      name,
      greet,
      updateName,
    };
  }
}
</script>



<style>
.name{
  color: blue;
}
</style>