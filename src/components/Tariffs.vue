<script>
import Tariff from './Tariff.vue';
import SectionFooter from './SectionFooter.vue';
const sectionName = "tariffs";
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
  components: { Tariff, SectionFooter },
  data() {
    return {
        sectionName,
        format: "webp",
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
      ],
      tariffsTitle: [
        "LITE (САМОСТОЯТЕЛЬНЫЙ)",
        "PLUS (С КУРАТОРОМ)",
        "BOMBA (С ЮЛИЕЙ ВОРМАН)"
      ],
      tariffsPrice: [
        "6666",
        "11111",
        "33333"
      ]
  }
    }
    }
</script>
<template>
    <section :class="sectionName" :id="sectionName" ref="sectionRef" >
        <div class="tariiffs__container container">
          <h2 class="title">ТАРИФЫ УЧАСТИЯ</h2>
          <div class="tariiffs-cards">
            <Tariff v-for="(i, index) in 3" :tariffsTitle="tariffsTitle[index]" :tariffsPrice="tariffsPrice[index]" :tariff="tariffsTxt" :tariffsIndex="index" :sectionName="sectionName" :tariffsImg="`${sectionName}/${tariffsImg[index].src}.${format}`"/>
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
  row-gap: 7rem

.container
  flex-direction: column
  gap: 3.3rem

</style>