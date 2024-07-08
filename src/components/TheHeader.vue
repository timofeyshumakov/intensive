<script>
import HeaderList from './HeaderList.vue';
const sectionName = "header";
export default {
  components: { HeaderList },
  data() {
    return {
        sectionName,
        litem: [
        {txt: "ДЛЯ КОГО?", link: "#"},
        {txt: "ЧТО БУДЕТ НА ИНТЕНСИВЕ?", link: "#"},
      {txt: "О ЮЛИИ", link: "#"},
      {txt: "ТАРИФЫ", link: "#"}
        ],
    }
    }
}
</script>



<template>
    <header class="header">
      <div class="container">
        <h1>ИНТЕНСИВ <span>ЮЛИИ ВОРМАН</span></h1>
        <nav>
          <HeaderList :litem="litem" :sectionName="sectionName"/>
        </nav>
      </div>
    </header>
</template>

<style scoped lang="sass">
@import "../vars.sass"

h1
  font-size: 1rem
  font-weight: 400
  color: $white

h1 span
  display: block

.header
  padding-top: 8rem
  width: 100%
  background: #4c3d74

.container
  flex-direction: row
  justify-content: space-between
  max-width: 82rem

.list
  display: flex
  gap: 3.6rem
  padding-right: 0.5rem
</style>
