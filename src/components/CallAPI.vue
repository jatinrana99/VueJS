<template>
    <h1>Here is a API</h1>

    <table>
        <tr>
        <th>Id</th>
        <th>First Name</th>
        <th>Last Name</th>
        <th>Email</th>
        <th>Profile Pictute</th>
        </tr>
        <tr v-for="obj in arr" :key="obj">
            <td>{{ obj.id }}</td>
            <td>{{ obj.first_name }}</td>
            <td>{{ obj.last_name }}</td>
            <td>{{ obj.email }}</td>
            <td><img :src="obj.avatar" alt=""></td>
        </tr>
    </table>

<section v-for="obj in arr" :key="obj" id="frame">
    <div class="img">
        <div><img :src="obj.avatar" alt=""></div>
    </div>
    <div class="details">
    <div>Id : {{ obj.id }}</div>
    <div>First Name : {{ obj.first_name }}</div>
    <div>Last Name : {{ obj.last_name }}</div>
    <div>Email : {{ obj.email }}</div>
    </div>
    

</section>


<section v-for="obj in arr" :key="obj" id="frame2">
    <div class="img">
        <div><img :src="obj.avatar" alt=""></div>
    </div>
    <div class="details2">
    <div>Id : {{ obj.id }}</div>
    <div>First Name : {{ obj.first_name }}</div>
    <div>Last Name : {{ obj.last_name }}</div>
    <div>Email : {{ obj.email }}</div>
    </div>
    

</section>

 
</template>

<script>
import axios from 'axios'
export default {
    name:`CallAPI`,
    data(){
        return{
            arr:[]
        }
    },
    async mounted(){
        let result = await axios.get("https://reqres.in/api/users?page=1");
        console.warn("hello ", result.data.data);
        this.arr= result.data.data
    }
}
</script>


<style scoped>
table{
    border: 2px solid;
    /* display: inline; */
}
td{
    border: 2px solid;
}

#frame{
    border: 2px solid;
    display: flex;
    margin: 6px;
    width: 482px;
    background-image: url('../assets/photo-1541701494587-cb58502866ab.avif');
   /* display: inline; */
}

#frame2{
    border: 2px solid;
    display: flex;
    margin: 6px;
    width: 482px;
    background-image: url('../assets/pre-printed-ayushman-bharat-card-1000x1000.webp');
    background-size: 499px 163px;
   /* display: inline; */
}

.details2{
    display: flex;
    flex-direction: column;
    justify-items: center;
    padding: 35px;
}

.details{
    display: flex;
    flex-direction: column;
    justify-items: center;
    padding: 35px;
    color: white;
}


.img{
    border: 2px solid;
    margin: 10px;
    
}
</style>