<template>
  <div id="app">
    <input type="text" v-model="newTask">
    <button @click="tasks.push({content: newTask, done: false})">Add</button>
    <div v-for="(task,index) in tasks" :key="index">
      <input type="checkbox" v-model="task.done">
      <span :class="{done: task.done}">{{task.content}}</span>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return {
      newTask:'',
      tasks: []
    }

  }
}
</script>

<style>
.done {
  text-decoration: line-through;
}
</style>
