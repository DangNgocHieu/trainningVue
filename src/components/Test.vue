<template>
  <div>
    <input v-model="message" placeholder="Nhập thông điệp" />
    <button @click="aa">Click me</button>
    <p>Thông điệp: {{ message }}</p>
  </div>
</template>
<script>
export default {
  data () {
    return {
      message: ''
    }
  }
}
</script>