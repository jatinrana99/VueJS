<template>
    <div>Hi I am Profile</div>
    <div>{{ profileName }}</div>
    </template>
    
    <script>
import { useRoute } from 'vue-router';

    export default {
        name:`Profile`,
        data(){
            return{
                profileName:''
            }
        },
        mounted(){
            let route=useRoute();
            console.warn("route" , route.params.name);
            this.profileName=route.params.name

        }
    }
    </script>