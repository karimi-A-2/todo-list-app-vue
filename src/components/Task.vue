<template>
    <div
        :class="[task.reminder ? 'reminder' : '', 'task']"
        @dblclick="$emit('toggle-task')"
    >
        <h3>{{task.text}}
            <i
                class="fas fa-times"
                @click="$emit('delete-task')"
            ></i>
        </h3>
        <p>{{task.day}}</p>
    </div>
</template>

<script>
export default {
    name: "Task",
    props: {
        task: Object,
    },
    emits: ["delete-task", "toggle-task"],
};
</script>

<style scope>
.task {
    background: #f4f4f4;
    margin: 5px;
    padding: 10px 20px;
    cursor: pointer;
}

.task.reminder {
    border-left: 5px solid green;
}

.task h3 {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.fas {
    color: red;
}
</style>