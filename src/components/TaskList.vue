<template>
  <div>TaskList</div>
  <div>
    <ul v-if="this.tasks.length > 0">
      <li v-for="(task, index) of tasks" :key="task.name">
        {{ task.name }}
        <button @click="() => deleteHandler(index)">Delete</button>
      </li>
    </ul>
    <h1 v-else>All Tasks Complete</h1>
  </div>
</template>

<script>
export default {
  name: "TaskList", 
  props: {
      tasks: Array,
      deleteHandler: Function
  },
};
</script>

<style></style>
