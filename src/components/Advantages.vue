<script>
import HeaderList from './HeaderList.vue';
import Img from './Img.vue';
const format ="svg";
const sectionName = "advantages";
export default {
  components: { HeaderList, Img },
  data() {
    return {
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
            {title: "1+ МЛН", txt: "В МЕСЯЦ ДЕЛАЮ НА РЕСНИЦАХ"},
            {title: "12+ ЛЕТ", txt: "РАБОТАЮ СВОЕЙ СФЕРЕ"},
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
                <HeaderList :litem="litem"/>
            </div>
            <div class="presentation">
                <div class="content">
                    <h2>И, КОНЕЧНО, ЮЛИЯ ВОРМАН</h2>
                    <div>БОЛЬШЕ 12 ЛЕТ Я НАРАЩИВАЮ РЕСНИЦЫ ЗА 1 ЧАС. В ПРОФЕССИ Я РАЗВИВАЮСЬ С 2008 ГОДА И, ПУТЕМ ПРОБ И ОШИБОК, ДОШЛА ДО ИДЕАЛЬНЫХ РЕЗУЛЬТАТОВ! МОИ ПРОФЕССИОНАЛЬНЫЕ НАВЫКИ СДЕЛАЛИ МЕНЯ МНОГОКРАТНЫМ ПРИЗЕРОМ, А ПОТОМ И СУДЬЕЙ МЕЖДУНАРОДНЫХ ЧЕМПИОНАТОВ ПО НАРАЩИВАНИЮ РЕСНИЦ</div>
                    <div>Я ОСНОВАЛА СЕТЬ САЛОНОВ VERSUS И ТЕПЕРЬ АКТИВНО ЗАПУСКАЮ СВОИ ОБУЧЕНИЯ ПО СКОРОМТНОМУ НАРАЩИВАНИЮ. ЛОМАЮ СТЕРЕОТИПЫ, УЧУ МАСТЕРОВ ПОДНИМАТЬ ЧЕКИ И ЗАРАБАТЫВАТЬ МИЛЛИОНЫ.</div>
                    <HeaderList :litem="list2"/>
                    <div>ВСЕ МОИ НАРАЩИВАНИЯ Я ДЕЛАЮ ЗА 1 - МАКСИМУМ 1.5 ЧАСА ХОЧЕШЬ ТАКЖЕ? СМОТРИ ПРОГРАММУ И ЗАПИСЫВАЙСЯ НА ИНТЕНСИВ</div>
                </div>
                <Img src="advantages/MARIA_LYADOVA.jpg"/>
            </div>
        </div>
    </section>
</template>
<style scoped lang="sass">

</style>