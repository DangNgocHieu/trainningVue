
<template>
  <div>
    <input v-model="message" placeholder="Nhập thông điệp" />
    <p>{{item }}</p>
    <button @click="aa">Submit</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      message: '',
      item :[],
    };
  },
  // watch: {
  //   message() {
  //     this.message = "";
  //   },
  // },
  methods: {
    aa() {
      this.item.push(this.message);
      this.message=""
    },
  },
};
</script>