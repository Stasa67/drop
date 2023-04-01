<template>
    <div class="footer-list-wrapper">
        <span class="caption-buyers">{{ title }}</span>
        <ul class="footer-list">
            <li class="footer-list__item" v-for="item in items" :key="item.message">
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
   }

   &-wrapper {
        width: 340px;
   }
}
 
</style>
