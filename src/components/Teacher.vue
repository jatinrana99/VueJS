<template>
    <h3>Teacher Data</h3>
    <!-- using the same data from the map components in teacher as well as in student class  -->
    The teacher name is {{ name }} {{ subject }}
</template>

<script>
export default {
    name:`Teacher`,
    props:{
        name:String,
        subject:String
    }
}
</script>