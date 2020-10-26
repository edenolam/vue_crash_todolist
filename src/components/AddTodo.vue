<template>
  <div>
    <form @submit="addTodo">
      <label>
        <input v-model="title" name="title" placeholder="Add todo" type="text">
      </label>
      <input class="btn" type="submit" value="submit">
    </form>
  </div>
</template>

<script>
export default {
  name: "AddTodo",
  data(){
    return{
      title:''
    }
  },
  methods: {
    addTodo(e){
      e.preventDefault();
      const newTodo = {
        title: this.title,
        completed: false
      }
      // send up to parent
      this.$emit('add-todo', newTodo);
      this.title = '';
    }
  }
}
</script>

<style scoped>
form {
  display: flex;
}

input[type="text"] {
  flex: 10;
  padding: 5px;
}

input[type="submit"] {
  flex: 2;
}
</style>
