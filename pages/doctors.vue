<script setup lang="ts">
const menu = ref()
const toggle = ({event}: { event: any }) => {
  menu.value.toggle(event)
}
const cards = ref([
  {
    id: 1,
    img: 'https://lorlor.ru/images/ci970607v360x540s0.jpg?state=98',
    name: 'Галкин Алексей Владимирович',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург',
    experience: '16 лет'
  },
  {
    id: 2,
    img: 'https://lorlor.ru/images/ci1155270v360x540s0.jpg?state=185',
    name: 'Садыхов Рагим Агаларович',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург',
    experience: '8 лет'
  },
  {
    id: 3,
    img: '/https://lorlor.ru/images/ci970605v360x540s0.jpg?state=133',
    name: 'Чуприков Роман Сергеевич',
    expert: 'эксперт по лор-патологиям',
    profession: 'оториноларинголог, ринохирург, фониатр, врач высшей категории',
    experience: '21 лет'
  },
  {
    id: 4,
    img: 'https://lorlor.ru/images/ci970605v360x540s0.jpg?state=133',
    name: 'Оганесян Тигран Сергеевич',
    expert: 'заведующий отделением, экс',
    profession: 'оториноларинголог, ринохирург',
    experience: '20 лет'
  },
  {
    id: 5,
    img: 'https://lorlor.ru/images/ci970618v360x540s0.jpg?state=77',
    name: 'Якушев Анатолий Андреевич',
    expert: 'ведущий врач клиники',
    profession: 'оториноларинголог, отохирург',
    experience: '13 лет'
  },
  {
    id: 6,
    img: 'https://lorlor.ru/images/ci1104163v360x540s0.jpg?state=113',
    name: 'Соколова Алла Васильевна',
    expert: 'кандидат медицинских наук',
    profession: 'оториноларинголог, отохирург, врач высшей категории',
    experience: 'свыше 35 лет'
  },
  {
    id: 7,
    img: 'https://lorlor.ru/images/ci1104163v360x540s0.jpg?state=113',
    name: 'Старосветский Андрей Борисович',
    expert: 'кандидат медицинских наук',
    profession: 'оториноларинголог, ринохирург',
    experience: '22 лет'
  },
  {
    id: 8,
    img: 'https://lorlor.ru/images/ci1104163v360x540s0.jpg?state=113',
    name: 'Мосейкина Лилия Алексеевна',
    expert: 'кандидат медицинских наук',
    profession: 'отохирург',
    experience: '31 лет'
  }
])

const products = ref([
      {
        id: '1000',
        title: 'Пройдите сурдологический комплекс!',
        description: 'Product Description',
        image: '/IMG/slider-1.png',
        link: ''
      },
      {
        id: '1001',
        title: 'Лор - операции',
        description: 'для иногородних',
        image: '/IMG/slider-2.jpg',
        link: 'узнайте подробнее'
      },
      {
        id: '1002',
        title: 'Безопасные лор - операции',
        description: 'лучшие лор - хирургии',
        image: '/IMG/slider-bg-1.jpg',
        link: 'узнайте подробнее'
      },
      {
        id: '1003',
        title: 'Поможем услышать мир',
        description: 'подбор и настройка слухавых аппаратов',
        image: '/IMG/slider-3.jpg',
        link: ''
      },
      {
        id: '1004',
        title: 'Пройдите информативный сурдологический комплекс!',
        description: '',
        image: '/IMG/slider-bg-2.jpg',
        link: ''
      },
      {
        id: '1005',
        title: 'Большая забота',
        description: 'детский лор - врач с огромным опытом работы',
        image: '/IMG/slider-bg-3.jpg',
        link: ''
      }
    ]
)
const responsiveOptions = ref([
  {
    breakpoint: '1400px ',
    numVisible: 1,
    numScroll: 1
  },
  {
    breakpoint: '991px',
    numVisible: 1,
    numScroll: 1
  },
  {
    breakpoint: '767px',
    numVisible: 1,
    numScroll: 1
  }
])
const getSeverity = ({status}: { status: any }) => {
  switch (status) {
    case 'INSTOCK':
      return 'success'

    case 'LOWSTOCK':
      return 'warning'

    case 'OUTOFSTOCK':
      return 'danger'

    default:
      return null
  }
}
</script>

<template>
  <section class="surface-300 bg-#F2F2F2">
    <div class="container">
      <div class="doctors__box">
        <div class="doctors__button1">Главная</div>
        <div class="doctors__button2">Специалисты</div>
      </div>
      <h1 class=" pt-8 mt48px font-semibold text-5xl">ЛОР-врачи</h1>
      <div class="grid">
        <div class="col:12 lg:col-4 mt36px">
          <div class="bg-white w-full pr-7">
            <div class="pt-4 pl-5">
              <h2>Филиал</h2>
              <div class="pb-2">
                <input type="radio" id="cat" name="caf">
                <label for="cat" class="pl-2 text-lg">Все филиалы</label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="radio" name="caf">
                  <span class="pl-2  text-lg">Преображенская площадь</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="radio" name="caf">
                  <span class="pl-2  text-lg">Бульвар Дмитрия Донского</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="radio" name="caf">
                  <span class="pl-2  text-lg">Мичуринский проспект</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="radio" name="caf">
                  <span class="pl-2  text-lg">Фили</span>
                </label>
              </div>
            </div>
            <div class="pt-4 pl-5">
              <h2>Направление врача</h2>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2  text-lg">Аллерголог-иммунолог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2  text-lg">Врач УЗИ</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2  text-lg">Выезд на дом</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Кардиолог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Массажист</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Медсестра</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Невролог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Отоларинголог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Отоневролог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Отохирург</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Психолог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Пульмонолог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Рефлексотерапевт</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Ринохирург</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Сурдолог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Терапевт</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Флеболог</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Фониатр</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2 text-lg">Эндокринолог</span>
                </label>
              </div>
            </div>
            <div class="pt-4 pl-5">
              <h2>Стиль работы</h2>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2  text-lg">Cтрогий доктор</span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2  text-lg">Доктор, с которым можно <br> <span
                      class="pl-5">поговорить как с партнёром</span></span>
                </label>
              </div>
              <div class="pb-2">
                <label>
                  <input type="checkbox" name="caf">
                  <span class="pl-2  text-lg">Понимающий и эмоциональный <br> <span class="pl-5">доктор</span> </span>
                </label>
              </div>
            </div>
          </div>
        </div>
        <div class="col:12 lg:col-8 mt29px">
              <div v-for="el in cards" :key="el.id" class="col-12 mb-6 pl-6 ">
                <div class=" card flex-column sm:flex-row flex p-4 bg-white w-full h-full">
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
          </div>
      </div>
  </section>
  <!--  <section class="bg-gray-100 pt-20">-->
  <!--    <div class="container">-->
  <!--      <h1 class="main-title main-title&#45;&#45;card mb-4">-->
  <!--        Наши специалисты-->
  <!--      </h1>-->
  <!--      <div class="grid -ml-6">-->
  <!--        <div v-for="el in cards" :key="el.id" class="col-12 xl:col-6 mb-6 pl-6 ">-->
  <!--          <div class=" card flex-column sm:flex-row flex p-4 bg-white w-full h-full">-->
  <!--            <div class="card-animation-left" />-->
  <!--            <div class="">-->
  <!--              <img class="card-img" :src="el.img" alt="">-->
  <!--            </div>-->
  <!--            <div class="ml-4 mt-5 ">-->
  <!--              <h1 class="card-name">-->
  <!--                {{ el.name }}-->
  <!--              </h1>-->
  <!--              <div class="card-job-title">-->
  <!--                <span>{{ el.expert }}</span>-->
  <!--              </div>-->
  <!--              <p class="main-description mt-4">-->
  <!--                {{ el.profession }}-->
  <!--              </p>-->
  <!--              <div class="main-description main-description&#45;&#45;bg-hover">-->
  <!--                <p>-->
  <!--                  стаж: <b>{{ el.experience }}</b>-->
  <!--                </p>-->
  <!--                <div class="rectangle" />-->
  <!--              </div>-->
  <!--              <div class="card-animation-right" />-->
  <!--            </div>-->
  <!--          </div>-->
  <!--        </div>-->
  <!--      </div>-->
  <!--      <div class="flex justify-content-center">-->
  <!--        <Button class="border-noround mr-3 border-0 p-tag-primary bg-cyan-700 hover:bg-cyan-600 text-xl" label="Задать вопрос врачу" />-->
  <!--        <Button class="border-noround ml-5 text-blue-700 hover:bg-blue-700 hover:text-white text-xl" label="Все специалисты" severity="success" outlined />-->
  <!--      </div>-->
  <!--      <p class="main-description mt-5 pb-6">-->
  <!--        Наши лор-врачи-->
  <!--        имеют огромный и уникальный опыт лечения лор-заболеваний, как взрослых пациентов, так и детей. У нас работает высокопрофессиональная команда отоларингологов высшей квалификационной категории, ринохирургов и отохирургов, в том числе 40% наших врачей имеют ученую степень кандидата медицинских наук. Наши специалисты ежедневно решают сложнейшие задачи и проводят уникальные-->
  <!--        хирургические операции-->
  <!--        лор-органов.-->
  <!--      </p>-->
  <!--    </div>-->
  <!--  </section>-->
</template>