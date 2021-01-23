<template>
  <div id="app">
    <div class="title">
      <h1>Today To-Do-List</h1>
    </div>
    <div class="hometask">
      <div v-for="myTask in task" v-bind:key="myTask.$index" class="task">
        <TaskList v-bind:myTask="myTask" />
      </div>
    </div>
  </div>
</template>

<script>
import TaskList from "./components/TaskList.vue";

export default {
  name: "App",
  data: function () {
    return {
      task: [
        {
          act: "Read a Book",
          isDone: false,
        },
        {
          act: "Manage Business",
          isDone: false,
        },
        {
          act: "Go Jogging",
          isDone: false,
        },
        {
          act: "Learn New Skill",
          isDone: false,
        },
      ],
    };
  },
  components: {
    TaskList,
  },
};
</script>

<style>
@import "../src/assets/style/style.css";
</style>
