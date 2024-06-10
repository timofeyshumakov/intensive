<script>
import Tariff from './Tariff.vue';
const format ="png";
const sectionName = "tariffs";
export default {
  components: { Tariff },
  data() {
    return {
        format: "png",
        sectionName: "tariffs",
        tariffsTxt: [
          {txt: "9 ПОДРОБНЫХ УРОКОВ"},
          {txt: "9 ЗАДАНИЙ НА ПОСТРОЕНИЕ СКОРОСТНОЙ РАБОТЫ"},
          {txt: "ЧАТ С ЕДИНОМЫШЛЕННИКАМИ"},
          {txt: "ДОПОЛНИТЕЛЬНЫЙ УРОК: ЛИЧНЫЙ БРЕНД ДЛЯ БЬЮТИ-СФЕРЫ"},
          {txt: "2 МАСТЕРМАИНДА С ЮЛИЕЙ ВОРМАН"},
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
            <Tariff v-for="(i, index) in 3" :tariff="tariffsTxt" :tariffsImg="`${sectionName}/${tariffsImg[index].src}.${format}`"/>
        </div>
    </section>
</template>
<style scoped lang="sass">

</style>