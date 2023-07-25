<template>
    <div>
        <input type="text" v-model="cari" placeholder="Cari Data">
        <ul>
            <li v-for="item in cariData" :key="item.id">
                    {{ item.title }} - {{ item.price }}
            </li>
        </ul>
        <p v-if="cariData.length === 0">Tidak Ada Pencarian</p>
    </div>
</template>
 
<script>
export default {
    data() {
        return {
            cari: "",
            products: []
        };
    },
       
        created(){
            this.products = [
                { id: 1, title: "Baju Anak", price: 75000 },
                { id: 2, title: "Baju Lansia", price: 38000 },
                { id: 3, title: "Celana Or", price: 48000 },
                { id: 4, title: "Hoodie ", price: 69000 },
                { id: 5, title: "Baju Crop Top", price: 28000 },
                
                ]
    },
    computed: {
        cariData() {
            return this.products.filter((item) => {
                return item.title.match(this.cari);
            });
                }
            }
        
    }
</script>