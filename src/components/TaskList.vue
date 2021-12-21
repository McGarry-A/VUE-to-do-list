<template>
  <div>TaskList</div>
  <div>
    <ul>
      <li v-for="task of tasks" :key="task.name">
        {{ task.name }}
        <button @click="deleteHandler">Delete</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "TaskList", 
  props: {
      tasks: Array,
  }
};
</script>

<style></style>
