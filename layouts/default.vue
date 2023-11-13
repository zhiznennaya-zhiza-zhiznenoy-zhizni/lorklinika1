<script setup lang='ts'>
import {useThemeStore} from '~/stores'

const themeStore = useThemeStore()

function toggleMenu() {
  var menu = document.querySelector('.menu');
  var menuWidth = menu.offsetWidth;

  if (menu.style.left === '0px') {
    menu.style.left = `-${menuWidth}px`;
  } else {
    menu.style.left = '0px';
  }
}

</script>

<template>
  <div>
    <section class="header mt-5">
      <div class="container">
        <div class="grid justify-content-center">
          <div class="xl:col-2 lg:col-12 pb-4">
            <div class="flex justify-content-center">
              <router-link to="/"><img class="h-30"
                                       src="https://lorklinika1.ru/content/images/logo.svg"></router-link>
            </div>
          </div>
          <div class="xl:col-7 lg:col-12 pb-4">
            <div class="">
              <h1 class="text-center text-2xl font-bold pb-4">КРУГЛОСУТОЧНАЯ ЛОР КЛИНИКА ДЛЯ ВЗРОСЛЫХ И ДЕТЕЙ</h1>
              <div class="flex justify-content-center">
                <div class="grid">
                  <div class="col-12 xl:col-4 sm:col-4 ">
                    <div class="block flex flex-column align-items-center justify-content-center ">
                      <div class="flex pro">
                        <div class=""><img class=" h-15px"
                                           src="data:image/png;base64,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"
                                           alt=""></div>
                        <p class="pl-2">Деловой центр</p>
                      </div>
                      <div class="flex pl-1 pro2">
                        <div class=""><img class=" h-15px"
                                           src="data:image/png;base64,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"
                                           alt=""></div>
                        <p class="pl-2 text-sm text-blue-900"> Москва-Сити, Башня «Империя»</p>
                      </div>
                    </div>
                  </div>
                  <div class="col-12 xl:col-4 sm:col-4 ">
                    <div class="block flex flex-column align-items-center justify-content-center ">
                      <div class="flex">
                        <div class=""><img class=" h-15px"
                                           src="data:image/png;base64,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"
                                           alt=""></div>
                        <p class="pl-2">Новые Черемушки</p>
                      </div>
                      <div class="flex pl-1 pro1">
                        <div class=""><img class=" h-15px"
                                           src="data:image/png;base64,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"
                                           alt=""></div>
                        <p class="pl-2 text-sm text-blue-900"> ул. Гарибальди, 3</p>
                      </div>
                    </div>
                  </div>
                  <div class="col-12 xl:col-4 sm:col-4 ">
                    <div class="block flex flex-column align-items-center justify-content-center ">
                      <div class="flex">
                        <div class=""><img class=" h-15px"
                                           src="data:image/png;base64,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"
                                           alt=""></div>
                        <p class="pl-2">Зюзино, Калужская</p>
                      </div>
                      <div class="flex pl-1">
                        <div class=""><img class=" h-15px"
                                           src="data:image/png;base64,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"
                                           alt=""></div>
                        <p class="pl-2 text-sm text-blue-900"> ул. Каховка, 37, корп.1</p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="xl:col-3 lg:col-12  ">
            <div class="text-center">
              <p class="text-center"><a href="tel:8 495 126-70-33;" class="text-4xl text-red-500 text-center">8 495
                126-70-33</a></p>
              <p class="text-red-500 text-lg text-center pt-3 ">общий колл-центр</p>
              <p class="pb-2 text-center">(круглосуточно)</p>
              <div class="text-center">
                <img class=" h-25px"
                     src="https://w7.pngwing.com/pngs/938/344/png-transparent-youtube-computer-icons-youtube-blue-text-trademark.png "
                     alt="">
                <img class="pl-1 h-25px" src="https://free-png.ru/wp-content/uploads/2022/02/free-png.ru-307.png "
                     alt="">
                <i class=" pl-1 pi pi-eye" style="font-size: 2rem; color: blue"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="bg-blue-100 mt-4 mb-8 pt-3 pb-3 none">
      <div class="slide__tell">
        <SpeedDial class="m20px fixed" :model="items" :radius="120" type="quarter-circle" direction="up-left"
                   :style="{ right: 0, bottom: 0 }"/>
      </div>
      <header class="">
        <div>
          <div class="line-box border-bottom-1 border-300">
            <div class="container">
              <div class="header__box flex justify-content-between align-items-center">
                <div class=" ">
                  <ul class="flex justify-content-between">
                    <li>
                      <router-link to="/" class="menu__items">Лор клиника</router-link>
                    </li>
                    <li>
                      <router-link to="/doctors" class="menu__items">Лор врачи</router-link>
                    </li>
                    <li>
                      <router-link to="/children" class="menu__items">Детский лор</router-link>
                    </li>
                    <li>
                      <router-link to="" class="menu__items">Пациентам</router-link>
                    </li>
                    <li>
                      <router-link to="/uslugi" class="menu__items">Услуги</router-link>
                    </li>
                    <li>
                      <router-link to="/prices" class="menu__items">Цены</router-link>
                    </li>
                    <li>
                      <router-link to="/reviews" class="menu__items">Отзывы</router-link>
                    </li>
                    <li>
                      <router-link to="/statyi" class="menu__items">Статьи</router-link>
                    </li>
                    <li>
                      <router-link to="/About__us" class="menu__items">О нас</router-link>
                    </li>
                    <li>
                      <router-link to="/contacts" class="menu__items">Контакты</router-link>
                    </li>

                  </ul>
                </div>
                <div class="flex align-items-center ">
                  <Button class="ml-3" icon="pi pi-user text-2xl" severity="secondary" rounded aria-label="Bookmark"
                          text/>
                  <Button class="header__icon ml-3" icon="pi pi-search text-2xl" severity="secondary"
                          rounded aria-label="Bookmark"
                          text/>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div>
        </div>
      </header>
    </section>
    <div class="container">
      <div>
        <div class="menu-btn" @click="toggleMenu">
          <div class="bar"></div>
          <div class="bar"></div>
          <div class="bar"></div>
        </div>

        <div class="menu" :style="{ left: menuVisible ? '0' : '-300px' }">
          <!-- Ваше меню здесь -->
          <ul>
            <li><a href="#">Главная</a></li>
            <li><a href="#">О нас</a></li>
            <li><a href="#">Контакты</a></li>
          </ul>
        </div>
      </div>
    </div>
    <Link rel="stylesheet" :href="themeStore.link"/>
    <slot/>
    <section>
      <footer class="bg-cyan-50 w-full pt-8 pb-7">
        <div class="container">
          <div class="grid">
            <div class="col-12 sm:col-6 xl:col-3 mb-4">
              <h2 class="text-xl font-semibold">
                Клиника
              </h2>
              <ul class="footer-menu">
                <li class="footer-item pb-2">
                  <router-link class=" text-black " to="">
                    Контакты
                  </router-link>
                </li>
                <li class="footer-item pb-2">
                  <router-link class=" text-black" to="">
                    О клинике
                  </router-link>
                </li>
                <li class="footer-item pb-2">
                  <router-link class=" text-black" to="">
                    Лор врачи
                  </router-link>
                </li>
                <li class="footer-item pb-2">
                  <router-link class=" text-black" to="">
                    Вакансии
                  </router-link>
                </li>
              </ul>
            </div>
            <div class="col-12 sm:col-6 xl:col-3 mb-4">
              <h2 class="text-xl font-semibold">
                Услуги
              </h2>
              <ul class="footer-menu">
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Прайс-лист
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Детский лор
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Дежурный лор
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Лор-врач на дом
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Онлайн-консультация
                  </router-link>
                </li>
              </ul>
            </div>
            <div class="col-12 sm:col-6 xl:col-3 mb-4">
              <h2 class="text-xl font-semibold">
                Пациентам
              </h2>
              <ul class="footer-item">
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Контроль качества
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Отзывы о лор-клинике
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Статьи
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Клинические случаи
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Прием по ДМС
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Налоговый вычет
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Бесплатное лечение
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Партнеры
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Отзывы на картах
                  </router-link>
                </li>
                <li class="pb-3">
                  <router-link class="text-black" to="">
                    Публичная оферта о компьютерной диагностике слуха
                  </router-link>
                </li>
              </ul>
            </div>
            <div class="col-12 sm:col-6 xl:col-3 ">
              <div class="flex  ">
                <div class="grid--branch-footer relative grid sm:justify-content-center flex-column">
                  <div class="branch-animation-left"/>
                  <div class="col-12 ">
                    <a href="tel:8 495 126-70-33" class=" text-black text-4xl font-bold ">8 495 126-70-33</a>
                    <p class=" text-lg font-semibold pt-2 text-black">
                      общий колл-центр
                    </p>
                    <p class=" text-lg  pb-4 text-black">
                      (круглосуточно)
                    </p>
                    <div class="flex ">
                      <div class=""><img class=" h-24px"
                                         src="../public/img/metro.svg.svg"
                                         alt=""></div>
                      <p class="metro__title text-lg">Деловой центр</p>
                    </div>
                    <p class="   pb-3  ">г.Москва, Москва-Сити, Башня «Империя»</p>
                    <div class="flex ">
                      <div class=""><img class=" h-24px" src="../public/img/metro.svg.svg" alt=""></div>
                      <p class="metro__title text-lg">Новые Черемушки</p>
                    </div>
                    <p class="pb-3">г.Москва, ул. Гарибальди, 3</p>
                    <div class="flex ghj">
                      <div class=""><img class=" h-24px" src="../public/img/metro.svg.svg" alt=""></div>
                      <p class="metro__title text-lg ">Зюзино,Калужская</p>
                    </div>
                    <p class=" pb-3 ">г.Москва, ул. Каховка, 37, корп.1</p>
                    <div class="branch-animation-right"/>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <p class="text-xl font-semibold text-black">Персональные данные</p>
          <p class="text-black pt-2 pb-2">Согласие на обработку персональных данных</p>
          <p class="text-black">Политика в отношении обработки персональных данных</p>
          <p class="text-black text-center pt-8 pb-3">© 2014 - 2023 ООО «ЛОР клиника плюс 1»</p>
          <p class="text-black text-center pb-3">Лицензия № ЛО-77-01-008196 от 07 мая 2014 г.</p>
          <p class="text-black text-center">Карта сайта</p>
        </div>
      </footer>
    </section>
  </div>
</template>
<style scoped>
.menu__items {
  color: #000;
  border-width: 4px 1px 1px 1px;
  border-style: solid;
  border-color: transparent;
  font-size: 16px;
  color: #333;
  font-family: "Roboto", sans-serif;
  margin-bottom: 0px;
  font-weight: 200;
  padding-left: 20px;
  padding-top: 300px;
}
.none{
  @media screen and (max-width: 1024px){
    display: none;
  }
}


.menu-btn {
  display: flex;
  flex-direction: column;
  cursor: pointer;
  padding: 15px;
}

.bar {
  width: 25px;
  height: 3px;
  background-color: #333;
  margin: 5px 0;
}

.menu {
  position: fixed;
  top: 0;
  left: -300px;
  width: 300px;
  height: 100%;
  background-color: #f1f1f1;
  transition: 0.3s;
}

.menu ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.menu li {
  margin: 15px;
}

.menu a {
  text-decoration: none;
  color: #333;
  font-size: 18px;
}
</style>