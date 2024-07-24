<script>
import HeaderList from './HeaderList.vue';
import Img from './Img.vue';
const format ="svg";
const sectionName = "advantages";
import { ref, onMounted } from 'vue'
export default {
  setup() {
    const sectionRef = ref(null)

    onMounted(() => {
      const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            setTimeout(() => {
              sectionRef.value.classList.add('fade-in')
            }, 100)
            observer.unobserve(entry.target)
          }
        })
      })
      observer.observe(sectionRef.value)
    })

    return {
      sectionRef,
    }
  },
  components: { HeaderList, Img },
  data() {
    return {
        sectionName,
        litem: [
            {txt: "9 УРОКОВ С ДОМАШНИМИ ЗАДАНИЯМИ И ПРОВЕРКОЙ", src: `${sectionName}/star-struck.${format}`},
            {txt: "МАСТЕРМАИНДЫ С ОБСУЖДЕНИЕМ ВОПРОСОВ", src: `${sectionName}/smiling-face-with-heart-eyes.${format}`},
            {txt: "ДЕЛЕНИЕ НА ПАРЫ И СОЗДАНИЕ АКТИВНОГО КОМЬЮНИТИ", src: `${sectionName}/money-mouth-face.${format}`},
            {txt: "ГЛАВНЫЙ ПРИЗ ЗА АКТИВНОСТЬ НА ИНТЕНСИВЕ", src: `common/gift.${format}`},
            {txt: "ПРИЗ ЗА РАБОТУ ДЛЯ САМОЙ АКТИВНОЙ ПАРЫ", src: `common/gift.${format}`},
            {txt: "ПРИЗ СРЕДИ СТОРИС С ХЕШТЕГОМ ИНТЕНСИВА ", src: `common/gift.${format}`}
        ],
        list2: [
            {title: "1 ЧАС", txt: "САМОЕ БЫСТРОЕ 5D"},
            {title: "12+ ЛЕТ", txt: "РАБОТАЮ СВОЕЙ СФЕРЕ"},
            {title: "1+ МЛН", txt: "В МЕСЯЦ ДЕЛАЮ НА РЕСНИЦАХ"},
            {title: "100000+", txt: "КЛИЕНТОК Я ОСЧАСТЛИВИЛА"}
        ]
    }
    }
}

</script>
<template>
    <section :class="sectionName" :id="sectionName" ref="sectionRef">
        <div class="container">
            <div class="list__container">
                <h2 class="advantages__title title">НА ИНТЕНСИВЕ ТЕБЯ ЖДЕТ</h2>
                <HeaderList :litem="litem" :sectionName="sectionName"/>
            </div>
            <div class="presentation">
                <h2 class="presentation__title title">И, КОНЕЧНО, ЮЛИЯ ВОРМАН</h2>
                <div class="presentation__content">
                    <div class="content__txt">
                        <div class="txt">БОЛЬШЕ 12 ЛЕТ Я НАРАЩИВАЮ РЕСНИЦЫ ЗА 1 ЧАС. В ПРОФЕССИ Я РАЗВИВАЮСЬ С 2008 ГОДА И, ПУТЕМ ПРОБ И ОШИБОК, ДОШЛА ДО ИДЕАЛЬНЫХ РЕЗУЛЬТАТОВ! МОИ ПРОФЕССИОНАЛЬНЫЕ НАВЫКИ СДЕЛАЛИ МЕНЯ МНОГОКРАТНЫМ ПРИЗЕРОМ, А ПОТОМ И СУДЬЕЙ МЕЖДУНАРОДНЫХ ЧЕМПИОНАТОВ ПО НАРАЩИВАНИЮ РЕСНИЦ</div>
                        <div class="txt">Я ОСНОВАЛА СЕТЬ САЛОНОВ VERSUS И ТЕПЕРЬ АКТИВНО ЗАПУСКАЮ СВОИ ОБУЧЕНИЯ ПО СКОРОМТНОМУ НАРАЩИВАНИЮ. ЛОМАЮ СТЕРЕОТИПЫ, УЧУ МАСТЕРОВ ПОДНИМАТЬ ЧЕКИ И ЗАРАБАТЫВАТЬ МИЛЛИОНЫ.</div>
                        <HeaderList :litem="list2" sectionName = "presentation"/>
                        <div class="txt last">ВСЕ МОИ НАРАЩИВАНИЯ Я ДЕЛАЮ ЗА 1 - МАКСИМУМ 1.5 ЧАСА ХОЧЕШЬ ТАКЖЕ? СМОТРИ ПРОГРАММУ И ЗАПИСЫВАЙСЯ НА ИНТЕНСИВ</div>
                    </div>
                    <Img class="presentation__main-img" src="advantages/MARIA_LYADOVA.webp" alt="Юлия Ворман"/>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped lang="sass">
    
.list__container
    width: 100%
    display: flex
    flex-direction: column
    gap: 2.4rem

.list
    display: grid
    row-gap: 2rem
    font-size: 1.15rem
    column-gap: 1rem

.item
    display: flex
    gap: 2rem

h2
    text-align: center
    
.advantages__
    
    &title
        margin-left: 1rem

.presentation
    display: flex
    flex-direction: column
    gap: 0.8rem

.presentation__list
    row-gap: 1.7rem
    grid-template-columns: 1fr 1fr

.presentation__
    
    &title
        margin-top: -0.5rem
        margin-left: -19%

    &content
        display: grid
        grid-template-columns: 1fr 0.6fr
        max-width: 83rem
        gap: 1.5rem
        justify-content: flex-start
        align-items: center
        margin-top: 1.3rem

    &main-img
        width: 100%
        max-width: 400px

.container
    gap: 11rem

.txt
    max-width: 678px
    font-size: 1.15rem
    line-height: 1.5

.last
    max-width: 505px
    margin-top: -2.4rem

.content__txt
    display: flex
    flex-direction: column
    gap: 3.8rem

@media screen and (max-width: 912px)

    .presentation__
        
        &content
            grid-template-columns: 1fr
            grid-template-rows: 1fr
            align-items: center
            justify-content: center
            justify-items: center

        &title
            margin: 0

    .presentation .advantages__item
        align-items: center

    .container
        gap: 7rem

@media screen and (max-width: 360px)

    .container
        gap: 5rem
</style>