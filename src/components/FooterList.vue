<template>
    <div>
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
        title: String
    },
    computed: {
        items() {
            return [ 
            { message: 'Продавайте на Wildberries' },
            { message: 'Франшизный пункт выдачи' },
            { message: 'Перевозчикам' },
            { message: 'Партнерский пункт выдачи' } 
            ]
        }
        
    }
}

</script>

<style>
.caption-buyers {
   font-size: 18px;
   color: #FFFFFF;
}

.footer-list {
   padding: 0;
   list-style: none;
}

.footer-list__item {
   cursor: pointer; 
}

.footer-list__item:hover {
   color: #FFFFFF
}
 
</style>
