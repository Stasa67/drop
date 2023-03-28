<template>
    <div class="categories__item">
       <img :src="img">
    </div>
       
</template>

<script>
export default {
    name: 'CategoryComponent',
    props: {
        img: String
    }
}
</script>

<style>


.categories__item {
    cursor: pointer;
    border-radius: 18px;
    overflow: hidden;
    width: 336px;
    height: 244px;
    background-color: #000000;
}

.categories__item:hover {
    width: 336px;
    height: 244px;
    transition: 2s;
    transform: scale(1.2);
    opacity: 0.7;
    } 
</style>
