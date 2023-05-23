<template>
    <div id="testing">
        {{name}} Testing
        <br/>
        <br/>

        <input type="text" v-model="name" />
    </div>
</template>


<script>
export default {
    name: 'TestJatin',
    data:  () => {
        return{
            name:  "Jatin"
        }
    }
};
</script>

<style>
#testing {height: 45px ;
    width : 102px}
</style>