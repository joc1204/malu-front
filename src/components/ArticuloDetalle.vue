<script setup>

defineProps(['title','body'])

</script>


<template>
<div class="card">
    <div class="card-body">
        <h5 class="card-title">{{title}}</h5>
        
        <p>{{body}}</p>
    </div>

</div>
</template>

<style>
    h5{
        color: blue;
    }
</style>