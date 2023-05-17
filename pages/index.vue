<template>
  <div>
    <h1>ToDoApp</h1>
    <AddTask @add="addTask" />
    <TaskNameList :task-name-list="taskNameList" @complete="completeTask" />
  </div>
</template>

<script setup lang="ts">
const taskNameList = ref<string[]>([]);
const addTask = (taskName: string) => {
  taskNameList.value.push(taskName);
}
const completeTask = (newTaskNameList: string[]) => {
  taskNameList.value = newTaskNameList;
}
</script>