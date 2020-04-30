<template>
    <div class="container list-group-flush">
        <Task v-for="task in tasks" :key="task">{{task}}</Task>
    </div>
</template>

<script>
import Task from './Task';

export default {
    props: ['tasks'],
    components: {
        Task
    }
}
</script>

<style scoped>

</style>
