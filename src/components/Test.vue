<template>
    <div id="testing">
        Hello {{name}}
        <br/>
        <br/>

        <input type="text" v-model="name" />
        <button >Clear</button>
        <button>Captial</button>
<!-- right now above buttons are not working  -->

        <h4>Email {{Email}}</h4>
        <h4>Mobile Number {{getMobile()}}</h4>

<!-- I have to values in get Mobile function but i want to use only one than I have to call the function and than that property -->
<!-- Same will be done with methods also -->
        <h4>Age {{ getMobile().age }}</h4>


<!-- here we are using the gender method -->
        <h4>Gender {{getGender()}}</h4>


 <!-- here i am using methods which will return dynamic values  -->

        <h4> (Person 1 )  Last name {{ getLastName("Sharma") }}</h4>


<!-- See here I am using same methods multiple times and in this i am also using data (property) which i am accepting in my methods -->
        <h4>(Person 2 )  Last name {{ getLastName("Singh","Email") }}</h4>


<!-- here i am using data() property in this method -->
        <h4>Person 3 Email {{ getLastName() }}</h4>
    </div>
</template>


<script>
export default {
    name: 'TestJatin',
    // 


    data:  () => {
        return{
            name:  "",
            Email : `jatin@123`,


            // passing a  function

            getMobile: function () {
                return {
                    mobile:45223,
                    age:63,
                }
                
            }
        }
    },
   // age: 45 can't define like this (for passing the data in a template)

    // for that we have to make a function


    // allData()   we can not do like this we have to pass data or states in data function only and it can be only one ... 
    //     {
    //     return {
    //     }
    //  }



// Creating a method -------------------------------------

methods: {

    getGender(){
        return "male"
    },

// This method will return the dynamic values 
    getLastName(name){
        return{ name,
// here i am using data(function value) in this method
         Email : this.Email
        }
    }
},

// methods: {
   
// }




    }
 
</script>

<style scoped>
 /* #testing {
    color: brown;
 } */
</style>