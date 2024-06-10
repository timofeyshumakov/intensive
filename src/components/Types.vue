<script>
import Img from './Img.vue';
import Button from './Button.vue';
import TypesCard from './TypesCard.vue';
import SectionFooter from './SectionFooter.vue';
const sectionName = "types";
const format = "svg";
export default {
  
  components: { Img, Button, TypesCard, SectionFooter},
  data() {
    return {
        sectionName: "types",
        cards: [
            {txt: "ЛАШМЕЙКЕР, КОТОРЫЙ ДЕЛАЕТ НАРАЩИВАНИЕ ДОЛЬШЕ ОДНОГО ЧАСА?", img:{src: `${sectionName}/1.${format}`}},
            {txt: "МАСТЕР, КОТОРЫЙ ХОЧЕТ ПОМЕНЯТЬ МЫШЛЕНИЕ О НАРАЩИВАНИИ РЕСНИЦ ", img:{src: `${sectionName}/2.${format}`}},
            {txt: "СПЕЦИАЛИСТ, КОТОРОМУ НЕОБХОДИМЫ ПОДДЕРЖКА И КОМЬЮНИТИ РЯДОМ", img:{src: `${sectionName}/3.${format}`}}
        ],
    }
    }
}
</script>
<template>
    <section class="promo">
      <div class="container">
    <h2>ТЕБЕ НА ИНТЕНСИВ ЕСЛИ ТЫ</h2>
    <div class="cards">
        <TypesCard v-for="card in cards" :card="card" />
    </div>
    <SectionFooter :sectionName = "sectionName" txt="ЗАРЯДИСЬ ЭНЕРГИЕЙ И СТАНЬ САМЫМ ЗНАМЕНИТЫМ МАСТЕРОМ СВОЕГО ГОРОДА"/>
</div>
    </section>
</template>
<style scoped lang="sass">
@import "../vars.sass"

.container
    flex-direction: column

.block
    display: flex
    width: 100%
    justify-content: space-between
</style>