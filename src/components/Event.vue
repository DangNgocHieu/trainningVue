<template>
  <div>
    <!-- <input v-model="message" placeholder="Nhập thông điệp" />
    <p v-for="item in items"  v-bind:key="item" >{{ item }}</p> -->
    <!-- <button @click="click">Submit</button> -->
    <!-- <app-test></app-test> -->

    <!-- Mảng -->
    <p>test prevent</p>
    <button type="submit">TestPrevent</button>
    <p>xem thông tin $event </p>
    <button v-on:click="warn('Chưa submit được form', $event)">InfoEvent</button>
    <p>test on click </p>
    <button v-on:click="counter += 1 ">Add 1</button>
    <p>The button above has been clicked {{ counter }} times.</p>
    <p>Test once</p>
    <button v-on:click.once="counter += 1 ">Add 1</button>
    <p>The button above has been clicked {{ counter }} times.</p>
    <p>Test stop</p>
    <div @click="alertHello">
        <button @click.stop="alertWelcome">CLick</button>
    </div>
    <p>Test key modifier</p>
    <input v-on:keyup.enter="submit">
    <p>test exact </p>
    <input @click.ctrl.exact="onClick">
     <p>test mouse middle</p>
    <input @click.middle="onClick">
</div>
</template>
<script>
// import Test from './components/Test.vue'
export default {
  data () {
    return {
      counter: 0
    }
  },
  methods: {
    warn: function (message, event) {
      // bây giờ chúng ta có thể truy xuất đến sự kiện DOM native
      if (event) event.preventDefault()
      alert(message  + '!');
      console.log(event);
    },
    sayWelcome() {
      alert(1)
    },
    alertHello() {
        alert('Hello')
    },
    alertWelcome() {
        alert('Welcome')
    },
    onScroll() {
        alert('scroll')
    },
    submit() {
        alert('bạn vừa ấn enter')
    },
    onClick() {
        alert('bạn vừa ấn phim...')
    }
  }
 
  // watch: {
  //   message() {
  //     this.message = "";
  //   },
  // },
  // methods: {
  //   click () {
  //     this.items.push(this.message)
  //     this.message = ' '
  //   }
  // },
  // components: {
  //   appTest: Test
  // }
}
</script>

