<template>
    <h3>Teacher Data</h3>
    <!-- using the same data from the map components in teacher as well as in student class  -->
    The teacher name is {{ name }} {{ subject }}

    <!-- <Student :getHobby = "getHobby" />
    <h1>{{ studentHooby }}</h1> -->
    
</template>

<script>
    // import Student from './Child.vue'
export default {
    name:`Teacher`,
    // components: {
    //     Student
    // },

    // data(){
    //     return{
    //         studentHooby:""
    //     }
    // },
    // methods :{
    //     getHobby(hobby){
    //         this.studentHooby = hobby
    //     }
    
    // },
    props:{
        name:String,
        subject:String
    }
}
</script>