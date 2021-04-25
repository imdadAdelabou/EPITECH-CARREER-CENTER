<template>
    <div id="typeJob">
        <label><input type="checkbox"/><span>{{content}}</span></label>
    </div>
</template>

<script>
    export default {
        name: "TypeJob",
        props: {
            content: String,
        },
    }
</script>

<style scoped>
    #typeJob {
        display: flex;
    }
    span {
        font-family: "Poppins";
        margin-left: 8px;
        font-size: 10px;
    }
</style>