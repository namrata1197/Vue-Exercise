<template>
<div>
  <p>{{message}}</p>
  <div>
  <button @click="clicked">Reverse Message</button>
  </div>
  <div>
  <input v-model="message">
  </div>
  <span v-if="!seen">Now you see me</span>
   <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
</div>
</template>

<script>
export default {
  name: "About",
  data: function () {
    return {
      message:"hello world ",
      seen:true,
      todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
    };
  },
  methods: {
    clicked: function () {
      this.message=this.message.split('').reverse().join('');
    }
  }
}
</script>

<style>
li{
  text-align: left
}
</style>