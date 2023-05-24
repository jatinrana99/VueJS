<template>

        <!-- using the same data from the map components in teacher as well as in student class  -->

    <h3>Student Data</h3>
    The Student name is {{ name }}
    <br>
    Subject is {{ subject }}
</template>

<script>
export default {
    name:`Student`,
    props:{
        name:String,
        subject:String
    }
}
</script>