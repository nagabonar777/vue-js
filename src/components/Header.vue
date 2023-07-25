<template>
    <div>
        <center><h1>{{ text }}</h1></center>
    </div>
    
</template>
<script>
export default {
    props:['text']
}
</script>

<style>
text{
    font-style: italic;
}
</style>