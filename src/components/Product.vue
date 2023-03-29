<template>
    <div class="products_cards">
        <div class="products_cards-picture">
            <img class="products_cards-picture-img" :src="product.img">
            <div class="cards-text-img">Быстрый просмотр</div>
        </div>
        <div class="products_cards-info">
            <div class="product-cards_price">
                <b class="product-cards_price-now">{{ product.price }}</b>
                <s class="product-cards_price-last">{{product.oldPrice}}</s>
            </div>
            <div class="products_cards-description">
                <p>{{ product.text }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductComponent',
    props: {
        product: Object,
    }
}
</script>

<style>
.products_cards-picture {
   display: flex;
   align-items: center;
   width: 168px;
   height: 170px;
   border-radius: 16px;
   overflow: hidden;
}

.products_cards-picture-img {
    width: 100%;
}

</style>
