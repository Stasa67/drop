<template>
    <div class="categories__item">
       <img :src="img" class="categories__item__img">
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
    opacity: 0.7;
    } 

    .categories__item__img:hover {
    transform: scale(1.2);
    transition: 2s;
    }
</style>
