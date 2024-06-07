<script setup>
import HeaderList from './HeaderList.vue'
</script>

<template>
    <footer :class="sectionName">
        <div :class="sectionName + '__container container'">
          <HeaderList v-for="item in items" :key="item.id" :litem="item" />
          <div>{{ item }}</div>
        </div>
    </footer>
</template>

<style scoped lang="sass">
@import "../vars.sass"

.footer
  padding: 9rem
  background: #251933

.container
  width: 100%
  display: grid
  grid-template-columns: 1fr 1fr 1fr

.list
  display: flex
  flex-direction: column
  gap: 0.75rem
  justify-content: space-between
  height: 100%

.list:nth-child(3)
  text-align: end

.list:nth-child(2)
  text-align: center

.link
  line-height: 1.5

</style>
<script>

export default {
  components: { HeaderList },
  data() {
    return {
      items: [
        [
          {txt: "ЮЛИЯ ВОРМАН", link: "#"},
          {txt: "ИНН:", link: "#"},
          {txt: "ОГРНИП:", link: "#"}
        ],
        [
          {txt: "НАВЕРХ", link: "#"},
          {txt: "Design by @kemfetka", link: "#"}
        ],
        [
          {txt: "ПОЛИТИКА КОНФИДЕНЦИАЛЬНОСТИ", link: "#"},
          {txt: "ДОГОВОР-ОФЕРТА", link: "#"},
          {txt: "СВЯЗАТЬСЯ С НАМИ", link: "#"}
        ],
      ],
      sectionName: 'footer'
  }
}
};

</script>