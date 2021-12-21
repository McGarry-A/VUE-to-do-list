<template>
  <div>TaskList</div>
  <div>
    <ul>
      <li v-for="(task, index) of tasks" :key="task.name">
        {{ task.name }}
        <button @click="() => deleteHandler(index)">Delete</button>
      </li>
    </ul>
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
