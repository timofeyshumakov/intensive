<script setup>
import List from './HeaderList.vue'
  const litem = [
    {txt: "ДЛЯ КОГО?", link: "#"},
    {txt: "ЧТО БУДЕТ НА ИНТЕНСИВЕ?", link: "#"},
    {txt: "О ЮЛИИ", link: "#"},
    {txt: "ТАРИФЫ", link: "#"}
  ]
  const props = {
    litem,
    className: "menu__list"
  }
</script>

<template>
    <header :class="sectionName">
      <div :class="sectionName + '__container container'">
        <h1>ИНТЕНСИВ <span>ЮЛИИ ВОРМАН</span></h1>
        <nav>
            <List v-bind="props"/>
        </nav>
      </div>
    </header>
</template>

<style scoped lang="sass">
@import "../vars.sass"

h1
  font-size: 1rem
  font-weight: 400
  text-transform: uppercase

h1 span
  display: block

.header
  padding-top: 8rem
  width: 100%
  background: $violet

.header__

  &container
    flex-direction: row

    justify-content: space-between

.list
  display: flex
  gap: 3.6rem
  padding-right: 0.5rem

.item
  text-transform: uppercase

.item:nth-child(2)
  padding-right: 2.1rem

</style>

<script>
export default {
  data() {
    return {
      sectionName: 'header'
    };
  },
};
</script>