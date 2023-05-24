<template>
    <h2>{{ name }}</h2>
    <!-- Here we are passing data as an object -->
    <h2>{{ user}}</h2>
    <h2>{{ user.email }}</h2>
    <button v-on:click="info()">Call From Parent function</button>

    <!-- HTML Binding  -->
    <h1>{{ text }}</h1>
    <!-- Here we are getting the text as it is . So , For that we are using HTML Tag -->

    {{ tag }}
    <div v-html="tag">

    </div>



    <!-- Class Binding -->

    <h3 class="bgColor">Hi Here we are Binding only one class Property</h3>
    <h3 :class="{textRed:colorfull , errPink:true}">Hello Developer</h3>
    <button v-on:click="colorfull=!colorfull">Click here to Change Text Color</button>
    <div :class="applyStyle">
        <h3>Class Binding</h3>
    </div>

</template>

<script>

export default {
    name:`Child`,
    data() {
        return{
            text:"Developer",
            tag:"<h1>Jatin Rana</h1>",
            // for class binding
            colorfull:true,
            rad:true
        }
    },
    props:{
        name: String,
        user: Object,
        info:Function
    },
    computed:{
        applyStyle(){
            return{
                textRed:this.colorfull , 
                errPink:true,
                rad:this.rad
            }
        }
    }
}
</script>

<style scoped>
h2{
    background-color: cadetblue;
}

.bgColor{
    background-color: cornflowerblue;
}
.textRed{
    color: darkmagenta;
}
.errPink{
    background-color: burlywood;
}
.rad{
    border-radius:50%;
}
</style>