<template>
  <div>
      <p>ádadadas</p>
      <li v-repeat="user in users">
        {{ user.name }} - {{ user.email }}
      </li>
  </div>
</template>
<script>
export default {
  data () {
    return {
      users: [
        { name: 'Foo Bar', email: 'foo@bar.com' },
        { name: 'John Doh', email: 'john@doh.com' }
      ]
    }
  }
}
</script>