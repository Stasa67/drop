<template>
   <div>
      <div class="violet-header">
         <div class="violet-header_container">
            <div class="violet-top">
               <div class="violet-top_left">
                  <span class="ru">Ru</span>
                  <span class="header-btn">
                     <span class="material-symbols-outlined icon-geo">
                        home_pin
                     </span>
                     <span class="voron">Воронеж</span>
                  </span>
                  <span class="free">Бесплатная доставка</span>
                  <span class="sell">Продавайте на Wildberries</span>
                  <span class="work">Работа на Wildberries</span>
               </div>
               <div class="violet-top_right">
                  <span>Сообщить о проблеме</span>
               </div>
            </div>
            <div class="violet-bottom">
               <div class="violet-bottom__burger-container">
                  <span class="material-symbols-outlined icon-burger">
                     density_medium
                  </span>
               </div>
               <div class="logotype">WILDBERRIES</div>
               <input class="search-input" type="text" placeholder="Я ищу...">
               <div class="violet-bottom__container">
                  <div class="container-addres">
                     <span class="material-symbols-outlined icon-geo icon-geo--second">
                        home_pin
                     </span>
                     <div class="violet-bottom__container__address">Адреса</div>
                  </div>
                  <div class="container-come">
                     <span class="material-symbols-outlined">
                        person
                     </span>
                     <div class="violet-bottom__container__come">Войти</div>
                  </div>
                  <div class="container-basket">
                     <span class="material-symbols-outlined">
                        shopping_cart
                     </span>
                     <div class="violet-bottom__container__basket">Корзина</div>
                  </div>
               </div>
            </div>
         </div>
      </div>
      <div class="main-header">
         <div class="main-header-container">
            <div class="main-header-hight">
               <div class="seasonal promotions">
                  <img class="promotions-big" src="https://images.wbstatic.net/bners1/big_presale_2810.jpg">
               </div>
               <div class="category">
                  <CategoryComponent v-for="(item, index) in category" :img="item.img" :key="index" />
               </div>
               <div class="bestsellers">
                  <p class="bestsellers_">Хиты продаж</p>
               </div>
               <div class="products_container">
                  <ProductComponent v-for="(item, index) in product" :product="item" :key="index" />
               </div>
            </div>
         </div>
      </div>
      <footer class="footer">
         <div class="footer-container">
            <div class="footer-container_buyers">
               <FooterListComponent v-for="(item, index) in footer" :title="item.title" :key="index"/>
               <span class="caption-buyers">Покупателям</span>
               <ul class="footer-list">
                  <li class="footer-list__iten">Как сделать заказ</li>
                  <li class="footer-list__iten">Способы оплаты</li>
                  <li class="footer-list__iten">Доставка</li>
                  <li class="footer-list__iten">Возврат товара</li>
               </ul>
            </div>
            <div class="footer-container_partners">
               <FooterListComponent v-for="(item, index) in footer" :title="item.title" :key="index"/>
            </div>
            <div class="footer-container_company">
               <span class="caption-buyers">Компания</span>
               <ul class="footer-list">
                  <li class="footer-list__iten">О нас</li>
                  <li class="footer-list__iten">Реквизиты</li>
                  <li class="footer-list__iten">Контакты</li>
                  <li class="footer-list__iten">Пресс-центр</li>
               </ul>
            </div>
            <div class="footer-container_social-network">
               <span class="caption-buyers">Мы в соцсетях</span>
               <ul class="footer-list">
                  <li class="footer-list__iten">Вконтакте</li>
                  <li class="footer-list__iten">Телеграм</li>
                  <li class="footer-list__iten">Одноклассники</li>
                  <li class="footer-list__iten">YouTube</li>
               </ul>
            </div>
         </div>
      </footer>
   </div>
</template>

<script>
import CategoryComponent from './components/Category.vue'
import ProductComponent from './components/Product.vue'
import FooterListComponent from './components/FooterList.vue'
export default {
   name: 'App',
   components: {
      CategoryComponent,
      ProductComponent,
      FooterListComponent
   },
   computed: {
      category: function () {
         return [{
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         }, {
            img: "https://images.wbstatic.net/bners1/desk_oshade_2210_UT.jpg"
         },]
      },

      product: function () {
         return [
            {
               img: "https://www.novochag.ru/upload/img_cache/c8e/c8e5aab81ddfc1698ef5e66aa5534b9d_ce_400x600x0x0_cropped_400x600.jpg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Товар очень хороший",
               title: "Быстрый просмотр"
            },
            {
               img: "https://static.galamart.ru/images_1000/3ZJ9RAD.jpg?t=1576757721",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Купи коня",
               title: "Быстрый просмотр"
            },
            {
               img: "https://uberdeal.ru/wp-content/uploads/2020/04/1980.jpg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Богатырский конь",
               title: "Быстрый просмотр"
            },
            {
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1665821410_post_51468_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Бери, не пожалеееешь",
               title: "Быстрый просмотр"
            },
            {
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1666960508_post_51803_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Щас такого не поют",
               title: "Быстрый просмотр"
            },
            {
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1666688409_post_51696_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Ловите ритм",
               title: "Быстрый просмотр"
            },
            {
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1666960508_post_51803_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Иии раз, раз, раз-два-три",
               title: "Быстрый просмотр"
            },{
               img: "https://uberdeal.ru/wp-content/uploads/2022/08/1661432107_post_49622_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Там диги дам",
               title: "Быстрый просмотр"
            },{
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1666783509_post_51730_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Тиги дам там там",
               title: "Быстрый просмотр"
            },{
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1666614907_post_51684_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Аааааа и аааааа",
               title: "Быстрый просмотр"
            },{
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1666340406_post_51604_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Аааааа и аааааа",
               title: "Быстрый просмотр"
            },{
               img: "https://uberdeal.ru/wp-content/uploads/2022/02/1644928808_post_45030_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Аааааа и аааааа",
               title: "Быстрый просмотр"
            },{
               img: "https://uberdeal.ru/wp-content/uploads/2022/10/1665732608_post_51441_thumbnail.jpeg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Аааааа и аааааа",
               title: "Быстрый просмотр"
            },{
               img: "https://cs5.pikabu.ru/post_img/2014/10/09/11/1412878322_2014414081.jpg",
               price: '2304p',
               oldPrice: "666666666p",
               text: "Аааааа и аааааа",
               title: "Быстрый просмотр"
            },
         ]

      },
      footer: function () {
         return [
         {
            title: "Партнерам"
         }
         ]
      }
   }
}

</script>

<style>
html {
   font-family: system, -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Segoe WP', Roboto, Ubuntu, Oxygen, Cantarell, 'Fira Sans', 'Helvetica Neue', Helvetica, 'Lucida Grande', 'Droid Sans', Tahoma, 'Microsoft Sans Serif', sans-serif;
}

body {
   margin: 0;
   background: linear-gradient(0deg, #481173, #c811aa);
}

.violet-header {
   padding: 0 32px;
   color: #FFFFFF;
}


.icon-geo {
   font-size: 16px;
}

.icon-geo--second {
   font-size: 24px;
}

.violet-header_container {
   width: 1476px;
   padding: 14px;
   margin: 0 auto;
}

.violet-top {
   display: flex;
   justify-content: space-between;
   font-size: 14px;
   padding-bottom: 4px;
}

.violet-top-left {
   line-height: 40px;
}

.ru {
   margin-right: 24px;
   cursor: pointer;
   color: rgba(255, 255, 255, .6);
}

.ru:hover {
   color: #FFFFFF;
}

.free {
   margin-right: 24px;
   cursor: pointer;
   color: rgba(255, 255, 255, 0.625);
}

.free:hover {
   color: #FFFFFF;
}

.sell {
   margin-right: 24px;
   padding: 4px 12px;
   background: #cb11ab linear-gradient(90deg, #bf5ae0, #a811da);
   border-radius: 40px;
   cursor: pointer;
}

.work {
   padding: 4px 12px;
   background-color: #ff636d;
   background-image: linear-gradient(90deg, #ff636d, #f88245 55%, #f3a720);
   border-radius: 40px;
   cursor: pointer;
}

.violet-top_right {
   line-height: 26px;
   padding: 4px 12px;
   background: #cb11ab;
   border-radius: 40px;
   cursor: pointer;
}

.header-btn {
   margin-right: 24px;
   cursor: pointer;
   color: rgba(255, 255, 255, .625);
}

.header-btn:hover {
   color: #FFFFFF;
}

.violet-bottom {
   display: flex;
   justify-content: space-between;
   font-size: 14px;
   align-items: center;
}

.icon-burger {
   font-size: 36px;
   color: rgba(255, 255, 255, .6);
}

.icon-burger:hover {
   cursor: pointer;
   font-size: 40px;
   color: #FFFFFF;
}

.violet-bottom__burger-container {
   height: 40px;
   width: 40px;
   display: flex;
   justify-content: center;
   align-items: center;
}

.logotype {
   font-size: 50px;
   font-weight: 500;
}

.search-input {
   width: 732px;
   vertical-align: middle;
   white-space: nowrap;
   position: relative;
   background-color: rgba(240, 231, 240, 0.2);
   color: #FFFFFF;
   width: 47%;
   padding: 14px 120px 16px 44px;
   margin: 0;
   border-radius: 56px;
   border: none;
}

.search-input::placeholder {
   color: #FFFFFF;
}

.violet-bottom__container {
   display: flex;
   justify-content: space-between;
   font-size: 14px;
   align-items: center
}

.violet-bottom__container__address {
   cursor: pointer;
   color: rgba(255, 255, 255, 0.625);
}

.violet-bottom__container__address:hover {
   color: #FFFFFF;
}

.violet-bottom__container__come {
   cursor: pointer;
   color: rgba(255, 255, 255, 0.625);
}

.violet-bottom__container__come:hover {
   color: #FFFFFF;
}

.violet-bottom__container__basket {
   cursor: pointer;
   color: rgba(255, 255, 255, 0.625);
}

.violet-bottom__container__basket:hover {
   color: #FFFFFF;
}

.container-addres {
   display: flex;
   flex-direction: column;
   align-items: center;
   margin-right: 24px;
}

.container-come {
   display: flex;
   flex-direction: column;
   align-items: center;
   margin-right: 24px;
}

.container-basket {
   display: flex;
   flex-direction: column;
   align-items: center;
   margin-right: 24px;
}

.main-header {
   border-radius: 26px;
   padding: 50px 0;
   margin: 0 auto;
   width: 1476px;
   background-color: #FFFFFF;
}

.main-header-hight {
   display: block;
   padding: 22px
}

.promotions-big {
   border-radius: 14px;
   cursor: pointer;
   width: 100%;
}

.main-header-categories {
   display: grid;
   grid-template-columns: repeat(4, 1fr);
   font-size: 14px;
   padding: 54px 0;
   gap: 40px;
}

@media screen and (max-width: 900px) {
   .main-header-categories {
      grid-template-columns: repeat(2, 1fr);
   }
}

.category {
   display: grid;
   grid-template-columns: repeat(4, 1fr);
   font-size: 14px;
   padding: 54px 0;
   gap: 24px;
}

.bestsellers {
   display: flex;
   width: 95%;
   padding: 40px 0 1px;
   font-size: 31px;
   font-weight: 500;
}

.bestsellers_ {
   cursor: default;
}

.products_container {
   display: grid;
   grid-template-columns: repeat(7, 1fr);
   font-size: 14px;
   gap: 40px;
}

.cards-picture {
   cursor: pointer;
   width: 100%;
}

.product-cards_price-now {
   font-size: medium;
   padding-left: 12px;
}

.footer {
   position: relative;
   width: 1476px;
   margin: 0 auto;
}

.footer-container {
   display: flex;
   justify-content: space-between;
   flex-wrap: nowrap;
   align-items: center;
   padding: 36px;
   color: rgba(255, 255, 255, 0.625);
   cursor: default;
}

.caption-buyers {
   font-size: 18px;
   color: #FFFFFF;
}

.products_cards-picture {
   display: flex;
   align-items: center;
   width: 168px;
   height: 170px;
   border-radius: 16px;
   overflow: hidden;
}

.cards-text-img {
   opacity: 0;
   position: absolute;
   margin-left: 40px;
   transition: 0.5s;
   font-size: 10px;
   background-color: rgba(168, 163, 163, 0.523);
   padding: 10px 5px;
   color: #ffffff;
   border-radius: 14px;
}

.products_cards-picture:hover .cards-text-img {
   opacity: 1;
}

.cards-text-img:hover {
   cursor: pointer;
   transform: scale(1.1);
}

.products_cards-description {
   padding-left: 12px;
}

.footer-list {
   padding: 0;
   list-style: none;
}

.footer-list__iten {
   cursor: pointer;
}

.footer-list__iten:hover {
   color: #FFFFFF
}</style>
