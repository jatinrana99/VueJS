<template>

    <!-- <h1>User Components</h1> -->
    <div>
        
    <h3>Employee Id  : {{ data.id }}</h3>
    <h3>Employee Name : {{ data.name }}</h3>
    <h3>Employee Email  : {{ data.email }}</h3>
        <button v-on:click="getName(data.name)">Alert Name</button>
    </div>

</template>


<script>
export default {
    name:`User`,
    props:{
        data:Object,
        getName:Function
    }
}
</script>

<style scoped>
 h1{
    background-color: brown;
 }
 div{
    background-color: aqua;
    padding: 10px;
    border-radius: 50%;
    border-bottom: 2px solid;
    margin-bottom: 20px;
 }
</style>