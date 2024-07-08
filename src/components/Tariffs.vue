<script>
import Tariff from './Tariff.vue';
import SectionFooter from './SectionFooter.vue';
const format ="png";
const sectionName = "tariffs";
export default {
  components: { Tariff, SectionFooter },
  data() {
    return {
        sectionName,
        format: "png",
        tariffsTxt: [
          {txt: "9 ПОДРОБНЫХ УРОКОВ"},
          {txt: "9 ЗАДАНИЙ НА ПОСТРОЕНИЕ СКОРОСТНОЙ РАБОТЫ"},
          {txt: "ЧАТ С ЕДИНОМЫШЛЕННИКАМИ"},
          {txt: "ДОПОЛНИТЕЛЬНЫЙ УРОК: ЛИЧНЫЙ БРЕНД ДЛЯ БЬЮТИ-СФЕРЫ"},
          {txt: "2 МАСТЕРМАИНДА С ЮЛИЕЙ ВОРМАН", mark: "-"},
          {txt: "ЛИЧНОЕ ВЕДЕНИЕ ОТ ЮЛИИ ВОРМАН"}
      ],
      tariffsImg: [
        {src: `1`},
        {src: `2`},
        {src: `3`},
      ]
  }
    }
    }
</script>
<template>
    <section class="tariiffs">
        <div class="container">
          <h2>ТАРИФЫ УЧАСТИЯ</h2>
          <div class="tariiffs-cards">
            <Tariff v-for="(i, index) in 3" :tariff="tariffsTxt" :tariffsIndex="index" :sectionName="sectionName" :tariffsImg="`${sectionName}/${tariffsImg[index].src}.${format}`"/>
          </div>
          <SectionFooter :sectionName = "sectionName" txt="ИДЕТЕ НА ИНТЕНСИВ? ВЫЛОЖИТЕ ОБ ЭТОМ СТОРИС-ШАБЛОН С ОТМЕТКОЙ ЮЛИИ ВОРМАН И ВАС БУДЕТ ЖДАТЬ РОЗЫГРЫШ ДОПОЛНИТЕЛЬНОГО ПОДАРКА!" />
        </div>
    </section>
</template>
<style scoped lang="sass">

.tariiffs-cards
  display: flex
  flex-direction: row
  flex-wrap: wrap
  justify-content: center
  gap: 3rem
  row-gap: 5rem

.container
  flex-direction: column
  gap: 3.3rem

.tariffs
  padding-bottom: 13.3rem
  
</style>