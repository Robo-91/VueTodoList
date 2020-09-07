<template>
    <h1>{{ appHeading }}</h1>
</template>

<script>
export default {
    data() {
        return {
            appHeading: 'Todo List'
        }
    }
}
</script>

<style scoped>
    h1 {
        padding: 1em 10px 1em 10px;
        border-radius: 10px;
        background-color: #5bc0de;
        color: white;
        margin: 1.5em 10px 1.5em 10px;
    }
</style>