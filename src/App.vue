<template>
  <div>
    <input v-model="message" placeholder="Nhập thông điệp" />
    <p v-for="item in items"  v-bind:key="item" >{{ item }}</p>
    <button @click="click">Submit</button>
  </div>
</template>
/* eslint-disable */
<script>
export default {
  data () {
    return {
      message: '',
      items: []
    }
  },
  // watch: {
  //   message() {
  //     this.message = "";
  //   },
  // },
  methods: {
    click () {
      this.items.push(this.message)
      this.message = ' '
    }
  }
}

</script>

