<template>
    <div class="container list-group-flush task-list">
        <Task v-for="(task, index) in tasks" @click.native="removeTask(index)" :key="index">{{task}}</Task>
    </div>
</template>

<script>
import Task from './Task';

export default {
    props: ['tasks'],
    components: {
        Task
    },
    methods: {
        removeTask(index) {
            this.$emit('taskRemoved', index);
        }
    }
}
</script>

<style scoped>
    .task-list {
        max-width: 800px;
    }
</style>
