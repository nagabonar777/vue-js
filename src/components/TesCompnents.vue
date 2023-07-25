<template>
    <div v-if="age > 18">
    <P>Selamt datang {{ name }}</P>     
    </div>
    <div v-else>
        <p>Maaf Kamu Belum Cukup Umur</p>
    </div>
    <button @click="greet">Sapa</button>
</template>
<script>
export default {
    props: ['name', 'age'],
    methods: {
    greet(){
        alert(" Halo " + this.name)
    }
        
    }
 }
</script>