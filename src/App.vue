<template>
  <div>
    <!-- <input v-model="message" placeholder="Nhập thông điệp" />
    <p v-for="item in items"  v-bind:key="item" >{{ item }}</p> -->
    <!-- <button @click="click">Submit</button> -->
    <!-- <app-test></app-test> -->

    <!-- Mảng -->
    <!-- <button type="submit">Submit</button>
    <button v-on:click="warn('Chưa submit được form', $event)"></button>
    <p>Words ban đầu:</p> 
    <li v-for="test in words" v-bind:key="test">{{ test }}</li>
    <button @click="click">Click me</button>
    <p>Mảng mới vị trí đầu tiên: {{ words[0] }}</p>
    <button v-on:click="counter += 1 ">Add 1</button>
    <p>The button above has been clicked {{ counter }} times.</p>
   <form id="demo">
  <p>
    <input type="text" v-model.lazy="msg" >
    {{msg}}
  </p>
   <p>
    <input type="number" v-model.number="msgnumber" >
    {{msgnumber}}
  </p>
   <p>
    <input type="text" v-model.trim="msgtrim" >
    {{msgtrim}}
  </p>
  <p>
    <input type="checkbox" v-model="checked">
    {{checked ? "yes" : "no"}}
  </p>
  <p>
    <input type="radio" name="picked" value="one" v-model="picked">
    <input type="radio" name="picked" value="two" v-model="picked">
    {{picked}}
  </p>
  <p>
    <select v-model="selected" >
      <option>one</option>
      <option>two</option>
    </select>
    {{selected}}
  </p>
  <p>
    <select v-model="multiSelect" multiple>
      <option>one</option>
      <option>two</option>
      <option>three</option>
    </select>
    {{multiSelect}}
  </p>
  <p><pre>data: {{$data | json 2}}</pre></p>
</form> -->
<app-event></app-event>
</div>
</template>
<script>
import Event from './components/Event.vue'
export default {
  data () {
    el: '#demo'
    return {
      // message: '',
      // items: [],
      // words : [{test:'spray'},{test:'spray12121'},{test:'hihieueu'},{test:'hihhieuieueu'},{test:'hihieuhieueu'} ],
      // result : [],
      // msgnumber:'',
      // msgtrim: '',
      // msg      : 'hi!',
      // checked  : true,
      // picked   : 'one',
      // selected : 'two',
      // multiSelect: ['one'],
      counter: 0
    }
  },
  methods: {
    // click() {
    //   this.words = this.words.filter(words => words.test.length >6)
    // },
    warn: function (message, event) {
      // bây giờ chúng ta có thể truy xuất đến sự kiện DOM native
      if (event) event.preventDefault()
      alert(message  + '!');
      console.log(event);
    },
    sayWelcome() {
      alert(1)
      }
  },
 
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
  components: {
    appEvent: Event
  }
}
</script>

