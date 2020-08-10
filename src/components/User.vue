<template>
  <div class="my-component">
    <div>{{ message.text }}</div>
    <div>
      <button @click="changeMessage">Click me</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: {
        type: "greeting",
        text: "How are you?",
      },
    };
  },
  methods: {
    changeMessage() {
      this.message.text = "this is new message";
    },
  },
  watch: {
    message: {
      handler: function () {
        console.log("something changed");
        console.log(this.message.type)
      },
      deep: true,
    },
  },
};
</script>


