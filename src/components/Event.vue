<template>
    <section class  = one  v-on:mousemove="getConsole()">
        <div>
            <h1>Events</h1>
        </div>
        <div>
            <h3>Welcome to Events Sections</h3>
        </div>
    </section>
    
    Click Button for Secret message
    <button v-on:click="alertMessage()">Click Me</button>

    
    <br>
    <br>
    <!-- Now we am passing the data in the method only -->
    <!-- Also you have to double click on it -->
    Double Click Button for Secret message
    <button v-on:dblclick="getdata('Hello user')">Get Data</button>
    
    <!-- Count Button -->
    <h2>{{ count }}</h2>
    <button  v-on:click="numCount()">Count</button>
</template>

<script>
export default {
    name:`Event`,
    data(){
        return{
            count:0
        }
    },
    methods: {
        alertMessage(){
            alert("Hello , Be HAPPY! , Everything will be Alright")
        },
        getdata(data){
            alert (data)
        },
        getConsole(){
            console.warn("Your mouse is in section area")
        },
        numCount(){
            this.count = this.count+1;
        }
    }
}
</script>
<style scoped>
.one{
    background-color: blue;
    color : palevioletred
}
</style>