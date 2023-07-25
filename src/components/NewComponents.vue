<template>
        <div>
            <Header text="Selamat anda dapat tiket surga"></Header>
            <MyComponents nama="Chandra" umur="20" alamat="Jl.Bandung"></MyComponents>
            <TesComponents name="Chandra" age="20"></TesComponents>
            <FooterComponets></FooterComponets>
            <TesDuaComponents></TesDuaComponents>
            <h2>Event Components</h2>
            <EventComponents :nama="nama" :umur="umur" :alamat="alamat" @greeted="onGreeted" >
                <template #footer>
                <div>
                    <p>Ini Adalah Footer Latihan Event</p>
                </div>
            </template>
            </EventComponents>
            
            <WatchersComponents nama="Konindina" umur="70"></WatchersComponents>
            
        </div> 
</template>

<script setup>
import EventComponents from './EventComponents.vue';
import FooterComponets from './FooterComponets.vue';
import MyComponents from './MyComponents.vue';
import TesComponents from './TesCompnents.vue';
import TesDuaComponents from './TesDuaComponents.vue';
import WatchersComponents from './WatchersComponents.vue';
import Header from './header.vue';
//event




</script>

<style>
</style>