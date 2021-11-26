<template>
  <div class="container">
  <header class="container">
    <h1 class="text-center">Input</h1>
  </header>
  <section class="container">
    <!-- Input fields -->
    <form
      @submit.prevent="addTodo"
      class="container max-w-lg rounded shadow-lg border-solid border-2 p-8"
    >
      <fieldset class="flex flex-col">
        <legend class="text-center"><h3>Add a new Task</h3></legend>
        <!-- Todo Title Input -->
        <label for="todo-title">Todo Title</label>
        <input type="text" name="todo-title" v-model="todo.title" />
        <!-- Todo Description Input  -->
        <label for="todo-descript">Todo Description</label>
        <input type="text" name="todo-descript" v-model="todo.descript" />
        <!-- This can use v-on as well -->
        <button>Add Item</button>
      </fieldset>
    </form>
  </section>
  </div>
</template>

<!--------------------------------SCRIPT-------------------------------->

<script>
export default {
  data() {
    return {
      todo: {
        title: "",
        descript: "",
      },
      todoItems: [],
    };
  },
  methods: {
    addTodo: function () {
      console.log(this.todo);
      return this.todoItems.push({
        title: this.todo.title,
        descript: this.todo.descript,
      });
    },
  },
};
</script>

<style>
  .container {
    display: flex;
    flex-direction: column;
  }
</style>