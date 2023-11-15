<template>
    <div class="footer-list-wrapper">
        <span class="caption-buyers">{{ title }}</span>
        <ul class="footer-list">
            <li class="footer-list__item" :class="item.type ? 'footer-list__item--' + item.type : ''" v-for="item in items"
                :key="item.message">
                {{ item.message }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'FooterListComponent',
    props: {
        title: String,
        items: Array
    }
}

</script>

<style lang="less">
.caption-buyers {
    font-size: 18px;
    color: #FFFFFF;
}

.footer-list {
    padding: 0;
    list-style: none;

    &__item {
        cursor: pointer;
        padding-top: 10px;

        &:hover {
            color: #FFFFFF
        }

        &--black {
            color: #000000;
        }

        &--red {
            color: #ff0000
        }

        &--green {
            color: #73ff00
        }

    }

    &-wrapper {
        width: 340px;
    }
}
</style>
