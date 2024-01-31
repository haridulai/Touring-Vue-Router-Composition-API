<script setup> 
import { useRouter } from 'vue-router';
const props = defineProps(["event"]); 
const router = useRouter()
const register = () => {
    // if registraction API call is successfull
    // push back to the event details
    router.push({
        name: 'EventDetails',
    })

    // Allows you to redirect without History, no going back to previous page
    // router.replace({
    //     name: 'EventDetails',
    // })
}
</script>

<template> 
    <p>Register for the event here</p> 
    <button @click="register">Register Me!</button>
</template>
