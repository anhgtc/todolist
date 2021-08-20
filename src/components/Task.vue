<template>
    <div class="form-check">
        <input type="checkbox" class="form-check-input" v-model="task.done">
        <label class="form-check-label" :class="{done: task.done}">{{task.name}}</label>
    </div>    
</template>

<script>
export default {
    props: ['task']
}
</script>

<style>
.done {
    text-decoration: line-through;
}
</style>