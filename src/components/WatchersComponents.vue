<template>
    <div>
        <h2 v-if="umur >= 18" >{{ pesanSelamat }}</h2>
        <p v-else>Maaf,Kamu belum cukup umur</p>
        <button @click="greet">Sapa Dulu Gak Sih</button>
    </div>
</template>

<script>
export default {
    props: ['nama', 'umur'],
    data() {
        return {
            pesan: 'halo, ' + this.nama + '!'
        };
    },
    methods: {
        greet() {
            alert('Hallo, Bro');
        }
    },
    computed:{
    pesanSelamat(){
            return 'Selamat datang, ' + this.nama + '!'
        }
    },
    watch: {
        umur(newUmur, oldUmur) {
            console.log('Umur berubah dari ',oldUmur,'menjadi ', newUmur)
        }
    }
    }
</script>
