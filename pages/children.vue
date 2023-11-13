<script lang="ts" setup>
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
  {
    id: 1,
    img: 'https://lorklinika1.ru/images/ci1142483v320x480s0.jpg?state=46',
    name: 'Тюрина Татьяна Олеговна',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург',
    experience: '16 лет'
  },


])
</script>
<template>
  <div class="container">
    <h1 class="text-4xl pl-5 font-semibold">Детский ЛОР врач в Москве</h1>
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
    <section><h1 class="font-semibold text-2xl">Детский лор-врач — это, прежде всего, опыт работы с детьми</h1>
    <p class="pb-4 text-base text-black ">Очень часто по телефону, при обращении в «ЛОР клиника плюс 1», задается
      вопрос: «У вас принимает детский
      лор-врач?»
    </p>
    <p class="pb-4 text-base text-black">По факту оториноларингология не подразделяется на возрастные группы (как это
      бывает в ряде других отраслей
      медицины, например, хирургии, кардиологии). То есть, будущие врачи-отоларингологи проходят обучение на одной
      кафедре: им всем читают одинаковые лекции и проводят одинаковые практические занятия и по взрослым, и по детским
      особенностям заболеваний уха, горла и носа.
    </p>
    <p class="pb-4 text-base text-black">Однако на практике картина иная. Если лор-врач на протяжении долгого времени
      работает только с детьми, он лучше
      находит с ними общий язык, знает, как помочь преодолеть боязнь и перевести ситуацию в игровую и позитивную. Также
      по мере накопления опыта ему все легче ориентироваться в особенностях протекания инфекционного процесса в детском
      возрасте, в дозировках препаратов, в том, как они переносятся в разном возрасте, как часто и какие бывают побочные
      эффекты.
    </p>
    <p class="pb-4 text-base text-black">Детский лор-врач быстро и умело проведет диагностику, не доставив ребенку
      дискомфорта. Безошибочно определит
      диагноз, потенциальные риски (возможность осложнений), с осторожностью назначит медикаментозную терапию, учитывая
      возраст и противопоказания.
    </p>
    <h1 class="font-semibold text-2xl">Детский лор-врач — это, прежде всего, опыт работы с детьми</h1>
    <p class="pb-4 text-base text-black">«ЛОР клиника плюс 1» оснащена для диагностики детей с самого рождения:</p>
    <ul class="list-menu">
      <li class="mt12px color-#F45B69 li3">
        <router-link class=" text-base text-black" to="/list">
          <p class="text-black">отоскопы и риноскопы различного размера для осмотра детей любого возраста;я</p>
        </router-link>
      </li>
      <li class="mt12px color-#F45B69 li3">
        <router-link class=" text-base text-black" to="/list">
          <p class="text-black">отоакустическая эмиссия для исследования слуха до 1 года;</p>
        </router-link>
      </li>
      <li class="mt12px color-#F45B69 li3">
        <router-link class=" text-base text-black" to="/list">
          <p class="text-black">аудиометр-импедансометр для изучения слуха от 1 года;</p>
        </router-link>
      </li>
      <li class="mt12px color-#F45B69 li3">
        <router-link class=" text-base text-black " to="/list">
          <p class="text-black pr-3">ультразвуковые приборы для исследования придаточных пазух носа, без дополнительной
            лучевой нагрузки устанавливающие воспаление в гайморовых и фронтальных пазухах.</p>
        </router-link>
      </li>
    </ul>
    <p class=" text-base text-black pt-4">В клинике есть профессиональное оборудование для аппаратного лечения. Многие
      методы, например, УЗОЛ-терапия, в части случаев позволяют купировать инфекционный воспалительный процесс без
      антибиотикотерапии, что актуально для часто болеющих детей. Лазеротерапия позволяет не только справиться с
      воспалением, но и значительно укрепить местный иммунитет в носоглотке, что важно для дошкольников и школьников.
    </p>
    <p class=" text-base text-black pt-4 pb-4">
      Оборудование для физиотерапии – это бесконтактные, безболезненные и очень эффективные приборы, не имеющие
      ограничений по возрасту.
    </p>
    <h1 class=" text-2xl"> <span class="font-semibold"> Записывайтесь</span> в «ЛОР клинику плюс 1»!</h1>
    <p class=" text-base text-black pt-4 pb-4">
      Наши отоларингологи с чуткостью настраивают ребенка на осмотр и лечение, а также учат родителей элементам терапии в домашних условиях. Совместными усилиями мы приводим ребенка к скорейшему выздоровлению.
    </p>
    </section>
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
  </div>
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
