<template>
  <div>
    <h1>Aplikasi Vue.js Gue</h1>
    <MyComponents
      :nama="nama"
      :umur="umur"
      :alamat="alamat"
      @greeted="onGreeted"></MyComponents>
  </div>
</template>

<script>
import MyComponents from './MyComponents.vue';

export default {
  components: {
    MyComponents,
    
},
  data() {
    return {
      nama: 'John',
      umur: 25,
      alamat:'Bandung'
    };
  },
  methods: {
    onGreeted() {
      alert('Kamu udah disapa, bro!');
    }
  }
}
</script>