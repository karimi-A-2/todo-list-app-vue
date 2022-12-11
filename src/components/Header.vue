<template>
    <header>
        <h1>{{ title }}</h1>
        <Button
            :text="isAddTask ? 'Add Task' : 'Close'"
            :color="isAddTask ? 'green' : 'red'"
            @btn-click="$emit('toggle-add-task')"
        />
    </header>
</template>

<script>
import Button from "./Button.vue";
export default {
    name: "Header",
    props: {
        title: {
            tyepe: String,
            default: "Hello World",
        },
        isAddTask: {
            tyepe: Boolean,
            default: true,
        },
    },
    components: {
        Button,
    },
    emits: ["toggle-add-task"],
};
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>