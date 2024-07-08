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
    <section class="types">
      <div class="container">
    <h2 class="header">ТЕБЕ НА ИНТЕНСИВ ЕСЛИ ТЫ</h2>
    <div class="cards">
        <TypesCard v-for="card in cards" :card="card" />
    </div>
    <SectionFooter :sectionName = "sectionName" txt="ЗАРЯДИСЬ ЭНЕРГИЕЙ И СТАНЬ САМЫМ ЗНАМЕНИТЫМ МАСТЕРОМ СВОЕГО ГОРОДА"/>
</div>
    </section>
</template>
<style scoped lang="sass">
@import "../vars.sass"

.header
    margin-right: 12rem

.container
    flex-direction: column
    gap: 3rem

.cards
    display: grid
    grid-template-columns: repeat(3, 1fr)
    gap: 6%
    margin-left: 2.8rem

@media screen and (max-width: 768px)
    .cards
        grid-template-columns: repeat(1, 1fr)
        max-width: 500px
        gap: 2.7rem

</style>