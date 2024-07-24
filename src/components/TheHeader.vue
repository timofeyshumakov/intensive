<script>
import HeaderList from './HeaderList.vue';
const sectionName = "header";
export default {
  components: { HeaderList },
  data() {
    return {
        isMobile: window.innerWidth < 767,
        isMenuOpen: false,
        sectionName,
        litem: [
        {txt: "ДЛЯ КОГО?", link: "#types"},
        {txt: "ЧТО БУДЕТ НА ИНТЕНСИВЕ?", link: "#programm"},
      {txt: "О ЮЛИИ", link: "#advantages"},
      {txt: "ТАРИФЫ", link: "#tariffs"}
        ],
    }
  },
  mounted() {
    window.addEventListener('resize', this.handleResize);
  },
  methods: {
    
    handleResize() {
      this.isMobile = window.innerWidth < 767;
      if (this.isMobile) {
        this.isMenuOpen = false;
      }else{
        this.isMenuOpen = true;
      }
    },
    toggleMenu() {
      if (this.isMenuOpen) {
        this.isMenuOpen = false;
      }else{
        this.isMenuOpen = true;
      }
    },
  },
};
</script>

<template>
    <header class="header" :class="{ 'burger-active' : isMenuOpen }">
      <div class="header__container container" :class="{ 'burger-active' : isMenuOpen }">
        <h1 :class="{ 'burger-active' : isMenuOpen }">ИНТЕНСИВ <span>ЮЛИИ ВОРМАН</span></h1>
        <div class="burger-container">
        <div v-if="isMobile" class="burger-menu" :class="{ 'burger-active' : isMenuOpen }" @click="toggleMenu">
          <span class="burger-line" v-for="i in 3"></span>
        </div>
        <nav v-if="isMenuOpen || isMobile === false " class="desktop-menu">
          <HeaderList :litem="litem" :sectionName="sectionName" :class="{ 'burger-active' : isMenuOpen }"/>
        </nav>
        </div>
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
  gap: 1rem

.list
  display: flex
  gap: 3.6rem

.burger-menu
  display: flex
  flex-direction: column
  gap: 0.45rem

.burger-line
  display: inline-block
  height: 0.2rem
  background: $white
  width: 2.86rem

@media screen and (max-width: 912px)

  .header
    padding-top: 6rem

@media screen and (max-width: 767px)

  .burger-menu.burger-active
    transform: translateX(10%)

  .burger-menu.burger-active .burger-line:nth-child(1)
    transform: rotate(45deg) translateY(200%)

  .burger-menu.burger-active .burger-line:nth-child(2)
    display: none

  .burger-menu.burger-active .burger-line:nth-child(3)
    transform: rotate(-45deg) translateY(-200%)

  .header.burger-active
    padding-top: 2rem
    position: fixed
    z-index: 10
    height: 100vh

  .header__container.burger-active
    gap: 2rem
    justify-content: center
    align-items: center
    flex-direction: column

  .header__list.burger-active
    align-items: center

  h1.burger-active
    text-align: center

  .header__list
    flex-direction: column
    align-items: flex-end
    gap: 1em

  .burger-container
    display: flex
    flex-direction: column-reverse
    gap: 2em
    align-items: center

</style>
