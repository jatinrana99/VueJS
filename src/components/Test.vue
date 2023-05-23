<template>
    <div id="testing">
        Hello {{name}}
        <br/>
        <br/>

        <input type="text" v-model="name" />
        <button >Clear</button>
        <button>Captial</button>


        <h4>Email {{Email}}</h4>
    </div>
</template>


<script>
export default {
    name: 'TestJatin',


    data:  () => {
        return{
            name:  "",
            Email : `jatin@123`
        }
    },



    // allData()   we can not do like this we have to pass data or states in data function only and it can be only one ... 
    //     {
    //     return {
    //     }
    //  }


    }
    // age: 45 can't define like this (for passing the data in a template)

    // for that we have to make a function
</script>

<style scoped>
 /* #testing {
    color: brown;
 } */
</style>