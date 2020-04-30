<template>
    <div class="list-group-item task fadeInLeft animated blue lighten-5">
        <p class="mb-0">
            <i class="fab fa-slack-hash fa-2x mr-4 mr-4 blue-gradient p-3 white-text rounded" aria-hidden="true"></i>
            <slot></slot>
        </p>
    </div>
</template>

<script>

</script>

<style scoped>
    .task:hover {
        cursor: pointer;
    }
    .task p {
        text-align: left;
    }
</style>
