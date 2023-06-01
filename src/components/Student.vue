<template>

        <!-- using the same data from the map.vue components in teacher as well as in student class  -->

    <h3>Student Data</h3>
    The Student name is {{ name }}
    <br>
    Subject is {{ subject }}


    <!-- <h4>Student Component</h4>

    <button v-on:click="getHobby(hobby)">Send Student Hobby </button> -->

    <!-- Its is a child -->

    <input type="text" ref="input">
    <button v-on:click="getInfo">Submit</button>
{{ getInfo().val }}
</template>

<script>
export default {
    name:`Student`,
    props:{
        name:String,
        subject:String,
        // getHobby:Function
    },
    // methods:{
    //     // getInfo(){
    //     //     return{
    //     //        val : this.$refs.input.value
    //     //     }
    //         this.$refs.input.focus();
    //         this.$refs.input.style.color="red";
    //         console.warn(val);
          

    //     }
    // }
}
    // data(){
    //     return {
    //         hobby:"Cricket"
    //         // to pass above property in parent (here it is teacher) we have to make a method (function) in pareent component only
    //     }
    // },
    // }


</script>

<style scoped>
h4{
    background-color: chartreuse;
}
</style>