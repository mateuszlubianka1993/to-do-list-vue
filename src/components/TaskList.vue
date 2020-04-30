<template>
    <div class="container list-group-flush">
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

</style>
