<template>
    <div>
        <task v-for="(task,index) in tasks" :key="index" :task="task"></task>
    </div>    
</template>

<script>
import Task from './Task.vue'
export default {
    components: { Task },
    props: ['tasks'] 
}
</script>
