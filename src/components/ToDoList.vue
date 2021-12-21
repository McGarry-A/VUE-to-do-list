<template>
  <div id="ToDoList">
    <form @submit.prevent="addTask()" id="input-area">
      <input type="text" placeholder="Task" v-model="newTask" />
      <button id="save-button" type="submit">Save</button>
    </form>
    <TaskList :tasks="tasks" />
  </div>
</template>

<script>
import TaskList from "./TaskList";

export default {
  name: "ToDoList",
  methods: {
    addTask() {
      return this.tasks.push({name: this.newTask})
    },
    removeTask() {},
    editTask() {},
  },
  components: {
    TaskList,
  },
  data: () => {
    return {
      newTask: "",
      tasks: [
        {
          name: "learn Vue",
        },
        {
          name: "Make counter app",
        },
        {
          name: "Make to do app",
        },
        {
          name: "build a website",
        },
      ],
    };
  },
};
</script>

<style>
#ToDoList {
  border: 4px solid #eee;
  display: flex;
  flex-direction: column;
  height: 800px;
  width: 500px;
  margin: 100px auto;
  border-radius: 10px;
  padding: 5em;
}

#input-area {
  margin: 60px auto;
}

#save-button {
  margin: 0 10px;
}

ul {
  list-style: none;
}

li {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
</style>
