<template>
    <div class="container list-group-flush task-list">
        <transition-group name="fade">
            <Task v-for="(task, index) in tasks" @click.native="removeTask(index)" :key="index">{{task}}</Task>
        </transition-group>
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
    .fade-enter {
        opacity: 0;
    }
    .fade-enter-active {
        animation: slide-in 0.7s ease-in-out forwards;
        transition: opacity 0.7s;
    }
    .fade-leave-active {
        animation: slide-out 0.7s ease-in-out forwards;
        transition: opacity 0.7s;
        opacity: 0;
    }
    
    @keyframes slide-in {
        from{
            transform: translateX(-80px);
        }
        to {
            transform: translateX(0);
        }
    }
    @keyframes slide-out {
        from{
            transform: translateX(0);
        }
        to {
            transform: translateX(-80px);
        }
    }
</style>
