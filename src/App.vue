<template>
  <div id="app">
    <Todos v-bind:todos="todos"></Todos>
  </div>
</template>

<script>
import Todos from "@/components/Todos";

export default {
  name: 'App',
  components: {
    Todos
  },
  data(){
    return {
      todos: [
        {
          id:1,
          title: "Todo ONE",
          completed: false
        },
        {
          id:2,
          title: "Todo TWO",
          completed: true
        },
        {
          id:3,
          title: "Todo THREE",
          completed: false
        },
      ]
    }
  }
}
</script>

<style>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body{
  font-family: Arial,sans-serif;
  line-height: 1.4;
}
</style>
