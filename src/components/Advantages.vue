<script>
import HeaderList from './HeaderList.vue';
import Img from './Img.vue';
const format ="svg";
const sectionName = "advantages";
export default {
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
    <section class="advantages">
        <div class="container">
            <div class="list-container">
                <h2>НА ИНТЕНСИВЕ ТЕБЯ ЖДЕТ</h2>
                <HeaderList :litem="litem" :sectionName="sectionName"/>
            </div>
            <div class="presentation">
                <h2 class="presentation-title">И, КОНЕЧНО, ЮЛИЯ ВОРМАН</h2>
                <div class="presentation-content">
                    <div class="content-txt">
                        <div class="txt">БОЛЬШЕ 12 ЛЕТ Я НАРАЩИВАЮ РЕСНИЦЫ ЗА 1 ЧАС. В ПРОФЕССИ Я РАЗВИВАЮСЬ С 2008 ГОДА И, ПУТЕМ ПРОБ И ОШИБОК, ДОШЛА ДО ИДЕАЛЬНЫХ РЕЗУЛЬТАТОВ! МОИ ПРОФЕССИОНАЛЬНЫЕ НАВЫКИ СДЕЛАЛИ МЕНЯ МНОГОКРАТНЫМ ПРИЗЕРОМ, А ПОТОМ И СУДЬЕЙ МЕЖДУНАРОДНЫХ ЧЕМПИОНАТОВ ПО НАРАЩИВАНИЮ РЕСНИЦ</div>
                        <div class="txt">Я ОСНОВАЛА СЕТЬ САЛОНОВ VERSUS И ТЕПЕРЬ АКТИВНО ЗАПУСКАЮ СВОИ ОБУЧЕНИЯ ПО СКОРОМТНОМУ НАРАЩИВАНИЮ. ЛОМАЮ СТЕРЕОТИПЫ, УЧУ МАСТЕРОВ ПОДНИМАТЬ ЧЕКИ И ЗАРАБАТЫВАТЬ МИЛЛИОНЫ.</div>
                        <HeaderList :litem="list2" :sectionName = "sectionName"/>
                        <div class="txt last">ВСЕ МОИ НАРАЩИВАНИЯ Я ДЕЛАЮ ЗА 1 - МАКСИМУМ 1.5 ЧАСА ХОЧЕШЬ ТАКЖЕ? СМОТРИ ПРОГРАММУ И ЗАПИСЫВАЙСЯ НА ИНТЕНСИВ</div>
                    </div>
                    <Img class="presentation-main-img" src="advantages/MARIA_LYADOVA.jpg"/>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped lang="sass">
.advantages
    padding-top: 12rem
    padding-bottom: 11.6rem
    
.list-container
    width: 100%
    display: flex
    flex-direction: column
    gap: 2.4rem

.list
    grid-template-columns: repeat(auto-fit, minmax(313px, 1fr))
    display: grid
    row-gap: 2rem
    font-size: 1.15rem
    column-gap: 1rem

.item
    display: flex
    gap: 2rem

h2
    text-align: center
    

.presentation
    display: flex
    flex-direction: column
    gap: 0.8rem

.presentation .advantages__list
    row-gap: 1rem

.presentation-title
    margin-top: -0.5rem

    advantages__list
.presentation-content
    display: flex
    width: 83rem
    gap: 3rem
    justify-content: flex-start

.presentation-title
    margin-left: -19rem

.presentation-main-img
    position: relative
    top: 3rem
    left: -1rem

.container
    gap: 11rem

.txt
    max-width: 678px
    font-size: 1.15rem
    line-height: 1.5

.last
    max-width: 505px
    margin-top: -3rem

.presentation-main-img
    margin: 3rem 0 0 -1rem

.content-txt
    display: flex
    flex-direction: column
    gap: 2.4rem


</style>