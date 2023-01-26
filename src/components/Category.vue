<template>
    <div>
        <div class="category">
            <div class="categories__item">
                <img :src="img">
            </div>
        </div>
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
.category {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    font-size: 14px;
    padding: 54px 0;
    gap: 40px;
}

.categories__item {
    cursor: pointer;
    border-radius: 18px;
    overflow: hidden;
    height: 244px;
    background-color: #000000;
}

.categories__item:hover {
    transition: 2s;
    transform: scale(1.2);
    opacity: 0.7;
}
</style>