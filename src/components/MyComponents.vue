<template>
    <div>
        <h1>Hallo Dunia</h1>
        <p> Nama :{{ nama }}</p>
        <p> Umur :{{ umur }}</p>
        <p> Alamat :{{ alamat }}</p>
    </div>
    <div>
        
    </div>
</template>


<script>

export default { 
    props:['nama','umur','alamat'],
    data() {
        return {
            message: "Ini pesam dari saya"
        }
    },
    methods: {
        greet() {
            console.log("Hallo")
        }
    }
 }
</script>

<style>
h1{
    color: black;
}

p{
    size: 16px;
}

</style>