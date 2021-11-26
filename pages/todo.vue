<template>
  <div class="container">
    <section>
      <ToDoForm @childToParent="retrieveToDos" />
    </section>
    
    <section class="container">
      <h2 class="text-center">Output</h2>
      <div>
        <ul class="container">
          <li
            v-for="todo in todoItems"
            :key="todo.id"
            class="border-solid border-2 my-4"
          >
            <h3 class="bg-gray-200 px-4">{{ todo.title }}</h3>
            <p class="p-4">{{ todo.descript }}</p>
          </li>
        </ul>
      </div>
    </section>

  </div>
</template>

<!-------------------------------- SCRIPT -------------------------------->

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
        description: this.todo.description,
      });
    },
  },
};
</script>
<style>


</style>