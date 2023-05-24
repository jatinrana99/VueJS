<template>
    <section class  = "one"  v-on:mousemove="getConsole()">
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

<!--                              -->


    <!-- here i am binding the property with two way binding -->
    <section class="one">
        <div>
             <h1>
                Get Input Field (Simple Form)
            </h1>
        </div>
        <input type="text" placeholder="Enter Email" v-model="email"/>
        <br>
        <br>
        <input type="password" placeholder="Enter Password" v-model="password"/>
        <br>
        <br>
        <button v-on:click="getFormData()" type="button">Get Values</button>
    </section>

    <section class="one">
        <div>
             <h1>
                Get Check Box and Radio Button Values 
            </h1>
        </div>
    </section>
    <h3>TECHNOLOGY</h3>
    <label for="java"> Java</label>
    <input type="checkbox" value="java" id="java" v-model="technology
    ">
    <label for="javascript"> Java Script</label>
    <input type="checkbox" value="javascript" id="javascript" v-model="technology
    ">
    <label for="php"> php</label>
    <input type="checkbox" value="php" id="php" v-model="technology
    ">
    <label for="vuejs"> Vue JS</label>
    <input type="checkbox" value="vuejs" id="vuejs" v-model="technology
    ">
    <label for="react"> React</label>
    <input type="checkbox" value="react" id="react" v-model="technology
    ">
    <br>
    <br>
    <br>

    <h3>Who you are ?</h3>
    <label for="student"> Student</label>
    <input type="radio" value="student" id="student"  name="profession" v-model="who">

    <label for="developer"> developer</label>
    <input type="radio" value="developer" id="developer" name="profession" v-model="who">


    <h4> Technology known by you {{ technology }}</h4>
    <h4>Profession {{ who }}</h4>
</template>

<script>
export default {
    name:`Event`,

    data(){
        return{
            count:0,
            email:null,
            password:null,
            technology:[],
            who:null
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
        },
        getFormData(){
            console.warn("values : ", this.email , this.password)
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