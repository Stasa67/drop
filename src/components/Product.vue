<template>
    <div class="products_cards">
        <div class="products_cards-picture">
            <img class="products_cards-picture-img" :src="product.img">
            <div class="cards-text-img">{{ product.title }}</div>
        </div>
        <div class="products_cards-info">
            <div class="product-cards_price">
                <b class="product-cards_price-now" :class="{ 'product-cards_price-now--green': product.oldPrice && !deleted }">
                    {{ resPrice }}р
                </b>
                <s class="product-cards_price-last" v-if="product.oldPrice && !deleted">
                    {{ resOldPrice }}р
                </s>
            </div>
            <div class="products_cards-description">
                <p>{{ product.text }}</p>
            </div>
            <div class="discount-button">
                <button v-if="product.oldPrice && !deleted" @click="() => deleteT()">Удалить скидку</button>
                <button v-if="product.oldPrice && deleted" @click="() => restoreT()">Вернуть скидку</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductComponent',
    props: {
        product: Object,
    },
    data () {
        return {
            deleted: false,
            dopPrice: 0,
            dopOldPrice: 0
        }
    },
    computed: {
        resPrice () {
            if (this.deleted) {
                return this.product.oldPrice + this.dopPrice
            }
            return this.product.price + this.dopPrice
        },
        resOldPrice () {
            if (this.deleted) {
                return this.product.price + this.dopPrice
            }
            return this.product.oldPrice + this.dopOldPrice
        }
    },
    methods: {
        deleteT () {
            this.deleted = true
            this.dopPrice += 100
            this.dopOldPrice -= 100
        },
        restoreT  () {
            this.deleted = false
        }
    }
}
</script>

<style lang="less">

.products_cards-picture {
   display: flex;
   align-items: center;
   width: 168px;
   height: 170px;
   border-radius: 16px;
   overflow: hidden;

   &-img {
    width: 100%;
   }
}

.product-cards_price {
    display: flex;
    justify-content: flex-start;
    padding-top: 8px;

    &-last {
        color: #ff0000;
        padding-left: 8px;
    }

    &-now--green {
        color: #27db27;
    }
}

.discount-button {
    display: flex;
    justify-content: center;
}
</style>
