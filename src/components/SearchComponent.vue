<template>
    <div id="search">
        <input type="text" id="input1" placeholder="Job title or keyword"/>
        <input type="text" id="input2" placeholder="Select Location"/>
        <button type="">Search</button>
    </div>
</template>

<script>
    export default {
        name: 'Search',
    }
</script>

<style scoped>
    #search {
        width: 50%;
        height: 50px;
        background-color: white;
        border-radius: 10px;
        display: flex;
        box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        margin: 45px 0px 0px 30px;
    }
    input {
        width: 30%;
        height: 50px;
    }
    #input1{
         border: none;
        background-color: transparent;
        outline: none;
    }
    #input2{
        border-style: none none none solid;
        outline: none;
        background-color: transparent;
        margin-right: 90px;
    }
    button {
        width: 30%;
        height: 40px;
        color: white;
        background-color: #db5669;
        border-radius: 10px;
        float: right;
        border: none;
        margin: 5px 10px 5px 0px;
        cursor: pointer;
        outline: none;
    }
</style>