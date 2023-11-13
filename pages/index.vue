<script setup lang="ts">
import {useThemeStore} from '~/stores'

const themeStore = useThemeStore()

import {Swiper, SwiperSlide} from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';

// import required modules
import {Pagination} from 'swiper/modules';


const modules = [Pagination];

const cards = ref([
  {
    id: 1,
    img: 'https://lorklinika1.ru/images/ci903450v320x480s0.jpg?state=85',
    name: 'Тюрина Татьяна Олеговна',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург',
    experience: '16 лет'
  },
  {
    id: 2,
    img: 'https://lorklinika1.ru/images/ci931890v320x480s0.jpg?state=40h',
    name: 'Мартынова Юлия Сергеевна',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург',
    experience: '8 лет'
  },
  {
    id: 3,
    img: 'https://lorklinika1.ru/images/ci844461v320x480s0.jpg?state=42',
    name: 'Жимолостнов Валентина Владимировна',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург, фониатр, врач высшей категории',
    experience: '21 лет'
  },
  {
    id: 4,
    img: 'https://lorklinika1.ru/images/ci844198v320x480s0.jpg?state=44',
    name: 'Янова Наталья Юрьевна',
    expert: 'заведующий отделением, экс',
    profession: 'оториноларинголог, ринохирург',
    experience: '20 лет'
  },
])
</script>
<template>
  <section class="mb-5">
    <div class="container mt-5">
      <router-link class="" to="">
        <h1 class="text-3xl text-blue-700 text-center underline pb-6">Безопасность пациента</h1>
      </router-link>
      <div class="grid justify-content-center">
        <div class="col-[20] ">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/video-conference.svg" alt="">
          </div>
          <p>Онлайн консультация</p>
        </div>
        <div class="col-[20]">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/24-hours.svg" alt="">
          </div>
          <p>Лор врач круглосуточно</p>
        </div>
        <div class="col-[20]">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/ambulance-new.svg" alt="">
          </div>
          <p>Вызов лор врача на дом</p>
        </div>
        <div class="col-[20]">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/baby-girl.svg" alt="">
          </div>
          <p>Детский лор врач</p>
        </div>
        <div class="col-[20]">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/sleep.svg" alt="">
          </div>
          <p>Слухопротезирование</p>
        </div>
        <div class="col-[20] pt-3">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/video-conference.svg" alt="">
          </div>
          <p>Лечение храпа</p>
        </div>
        <div class="col-[20] pt-3">
          <div class="flex align-items-center justify-content-center h-9rem w-9rem op border-circle">
            <img class="w-8" src="https://lorklinika1.ru/content/images/lp/heart.svg" alt="">
          </div>
          <p>Кардиология</p>
        </div>

      </div>
    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
  <section>
    <div class="container">
      <swiper
          :direction="'vertical'"
          :pagination="{
      clickable: true,
    }"
          :modules="modules"
          class="mySwiper"
      >
        <swiper-slide>
          <div class="adf1">

          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="adf">
          </div>
        </swiper-slide>
        <swiper-slide>Slide 3</swiper-slide>
        <swiper-slide>Slide 4</swiper-slide>
        <swiper-slide>Slide 5</swiper-slide>
        <swiper-slide>Slide 6</swiper-slide>
        <swiper-slide>Slide 7</swiper-slide>
        <swiper-slide>Slide 8</swiper-slide>
        <swiper-slide>Slide 9</swiper-slide>
      </swiper>
    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
  <section class="pt-5 pb-7">
    <div class="container">
      <h1 class="text-4xl font-semibold text-center">ЛОР клиника плюс 1</h1>
      <p class="pt-4 pb-2 text-lg">«ЛОР клиника плюс 1» - это многофилиальный лор-центр в Москве, 24 часа в сутки
        оказывающий помощь детям и
        взрослым с заболеваниями уха, горла и носа.</p>
      <p class=" pb-2 text-lg">Клиника оснащена отоларингологическим оборудованием от ведущих на медицинском рынке
        брендов. В сочетании с
        безупречной работой наших врачей это позволяет диагностировать лор-заболевания быстро и информативно.
        <span class="info__text">Врачи-оториноларингологи</span> проводят <span class="info__text">отоакустическую эмиссию</span>
        для детей до 1 года, <span class="info__text">эндоскопию,</span> <span
            class="info__text">отимпанометрию, </span> <span
            class="info__text">УЗИ
        придаточных пазух,</span> экспресс-диагностику на патогенный стрептококк с использованием <span
            class="info__text">стрептатеста,</span> и назначают
        комплексное лечение.</p>
      <p class=" pb-2 text-lg">Мы также проводим <span class="info__text">диагностику сна</span> аппаратом ApneaLink и
        <span class="info__text">лечение синдрома обструктивного
        апноэ сна</span> с помощью
        CPAP-терапии.</p>
      <p class=" pb-2 text-lg">В нашей клинике также проводится реабилитация после коронавируса, протекавшего без
        пневмонии или с пневмонией
        разной степени тяжести. Комплекс эффективных мероприятий, в том числе с использованием галокамеры, помогает
        восстановиться в кратчайшие сроки без осложнений. </p>
      <h1 class="text-4xl font-semibold">Обязательная видеоэндоскопия</h1>
      <p class=" pb-2 text-lg">Видеоэндоскопический осмотр лор-органов - непременный метод на приеме у врача. Он
        существенно повышает качество консультации, достоверность диагностики, правильность выставления диагноза и
        эффективность последующего лечения.</p>
    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
  <section class="pt-20">
    <div class="container">
      <h1 class="text-5xl font-semibold mb-4 text-center">
        Лор врачи
      </h1>
      <div class="grid -ml-6">
        <div v-for="el in cards" :key="el.id" class="col-12 xl:col-6 mb-6 pl-6 ">
          <div class=" card flex-column sm:flex-row flex p-4  w-full h-full" style="background-color: #F8FBFE;">
            <div class="card-animation-left"/>
            <div class="">
              <img class="card-img" :src="el.img" alt="">
            </div>
            <div class="ml-4 mt-5 ">
              <h1 class="card-name">
                <router-link to="">
                  {{ el.name }}
                </router-link>
              </h1>
              <div class="card-job-title">
                <span>{{ el.expert }}</span>
              </div>
              <p class="main-description mt-4">
                {{ el.profession }}
              </p>
              <div class="main-description main-description--bg-hover">
                <p>
                  стаж: <b>{{ el.experience }}</b>
                </p>
                <div class="rectangle"/>
              </div>
              <div class="card-animation-right"/>
            </div>
          </div>
        </div>
      </div>
      <div class="text-center ">
        <Button class=" ml-5 text-700 hover:bg-bluegray-700 hover:text-white text-xl border-round"
                label="Все специалисты" severity="success" outlined/>
      </div>
    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
  <section class="mt-7">
    <div class="container">
      <h1 class="text-4xl font-semibold text-center pt-2">Консультация ЛОР врача</h1>
      <p class=" pb-2 text-lg pb-3"><span class="info__text">Консультация ЛОР-врача</span> включает обязательный
        видеоэндоскопический осмотр ЛОР-органов, что существенно повышает
        качество консультации, достоверность диагностики, правильность и детализацию выставления диагноза и, как
        следствие, эффективность дальнейшего лечения.</p>
      <iframe class="w-full pb-4" height="642" src="https://www.youtube.com/embed/eSx2HjbqFB8"
              title="Лор клиника №1. Современная лор клиника в Москве." frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              allowfullscreen>
      </iframe>
      <h1 class="text-4xl font-semibold text-center pb-3">Современные методики лечения лор заболеваний</h1>
      <p class="text-lg">Мы проводим следующие процедуры физиотерапии:</p>
      <ul>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">УЗОЛ-терапия</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">фотохромотерапияФ</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">лазеротерапия</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">пневмомассаж</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">электрофорез</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">фонофорез</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">промывание лакун миндалин на аппарате «Тонзиллор»</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">магнитотерапия</p>
          </router-link>
        </li>
      </ul>
      <p class="text-lg pt-3">Для лечения гнойных синуситов, кроме традиционных методов, применяется метод
        ЯМИК-катетера
        для беспункционной борьбы с заболеванием.
      </p>
      <p class="text-lg pt-3">В клинике проводятся малоинвазивные хирургические вмешательства аппаратом «ФОТЕК»:</p>
      <ul class="pb-4">
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">подслизистая вазотомия</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2 text-black">удаление доброкачественных образований на слизистой носоглотки</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2">остановка носовых кровотечений</p>
          </router-link>
        </li>
        <li class="">
          <router-link class=" text-lg font-light" to="/list">
            <p class="li2 text-black">вапоризация лакун миндалин</p>
          </router-link>
        </li>
      </ul>
      <h1 class="text-4xl font-semibold text-center pt-2">Детский лор-врач</h1>
      <p class="text-lg pb-3">В детском возрасте лор-органы имеют свои специфические особенности строения. Их
        диагностика и лечение их
        заболеваний требует со стороны врача грамотного и продуманного подхода. Не менее важны внимательность и
        чуткость, с которыми детские отоларингологи должны обращаться со своими юными пациентами.</p>
      <p class="text-lg pb-3">В «ЛОР клинике плюс 1» маленьких пациентов ждут <span
          class="info__text">детские лор-врачи</span> с большим опытом работы
        с детьми, включая навыки эндоскопического осмотра у новорожденных. Мы стремимся сделать пребывание детей в
        клинике комфортным и приятным. Пока врач общается с родителями по вопросам лечения, они могут посмотреть
        мультфильмы, поиграть или порисовать в детском уголке.</p>
      <p class="text-lg pb-3">Заботясь о здоровье детей, наши <span
          class="info__text"> врачи-оториноларингологи</span>
        разработали программы по
        профилактическому консервативному лечению хронических аденоидитов и тонзиллитов у детей с предоставлением
        скидок. Клиника имеет огромный опыт <span class="info__text">лечения аденоидов без операции.</span></p>
      <h1 class="text-4xl font-semibold text-center pt-2">Лор круглосуточно</h1>
      <p class="text-lg pt-3 pb-6">«ЛОР клиника плюс 1» работает круглосуточно, включая праздничные и выходные дни,
        принимает взрослых и детей с
        самого рождения.</p>
      <h1 class="text-4xl font-semibold text-center pt-2">Вызов лор-врача на дом</h1>
      <p class="text-lg pt-4">Ежедневно до 20:00 вы можете вызвать нашего <span class="info__text">лор-врача к себе на дом.</span>
      </p>
      <p class="text-lg">Эта услуга удобна для тех пациентов, кто не может приехать в клинику в связи с плохим
        самочувствием или по
        причине загруженности своего времени.</p>
    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
  <section class="news w100% mt-5">
    <div class="container">
      <div class="news__title pt94px">
        <h1 class="text-4xl font-semibold pb-3">Новости</h1>
      </div>
      <div class="grid flex justify-content-center">
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1156474v480x320s0.jpg" alt="" class="news__img w100% h250px object-cover">
            <div class="news__block ml24px">
              <p class="text-red pt-4">
                23.08.2023
              </p>
              <p class="news__p mt16px pb-3">
                Повышение стоимости на часть медицинских услуг в сети "ЛОР клиника плюс 1"
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1156456v480x320s0.jpg" alt="" class="news__img object-cover w100% h250px">
            <div class="news__block ml24px">
              <p class="text-red pt-4">
                23.08.2023
              </p>
              <p class="news__p mt16px pb-3">
                Повышение стоимости на часть медицинских услуг в сети "ЛОР клиника плюс 1"
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1156422v480x320s0.jpg" alt="" class="news__img object-cover w100% h250px">
            <div class="news__block ml24px">
              <p class="text-red pt-4">
                23.08.2023
              </p>
              <p class="news__p mt16px">
                Повышение стоимости на часть медицинских услуг в сети "ЛОР клиника плюс 1"
              </p>
            </div>
          </div>
        </div>
      </div>
      <p class="text-right text-lg text-blue">все новости →</p>
    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
  <section class="articles w100% mt-5">
    <div class="container">
      <div class="news__title pt94px">
        <h1 class="text-4xl font-semibold pb-3">Статьи</h1>
      </div>
      <div class="grid flex justify-content-center">
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1156457v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold" >
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1155620v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Мифы в оториноларингологии
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1155148v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Хронический аденоидит и показания
                для аденотомии
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1155147v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1155145v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1154884v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1154686v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1154682v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 lg:col-4">
          <div class="news__blog   h-full bg-#FFF">
            <img src="https://lorklinika1.ru/images/ci1154681v480x320s0.jpg" alt="" class="object-cover w100% h250px">
            <div class="news__block ">
              <p class="news__p mt16px pb-3 text-xl font-semibold">
                Как научить ребенка сморкаться?
              </p>
            </div>
          </div>
        </div>
      </div>
      <p class="text-right text-lg text-blue">все статьи →</p>

    </div>
  </section>
  <!--/////////////////////////////////////////////////////////////////////////////////////-->
</template>
<style>


.swiper {
  width: 100%;
  height: 700px;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  background: #fff;

  /* Center slide text vertically */
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

</style>
