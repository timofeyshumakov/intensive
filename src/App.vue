<script setup>
import TheHeader from './components/TheHeader.vue';
import Promo from './components/Promo.vue';
import Types from './components/Types.vue';
import Advantages from './components/Advantages.vue';
import Programm from './components/Programm.vue';
import Tariffs from './components/Tariffs.vue';
import Faq from './components/Faq.vue';
import TheFooter from './components/TheFooter.vue';
import './reset.css';

</script>
<template>
  <div class="wrapper">
    <TheHeader/>
    <Promo/>
    <Types/>
    <Advantages/>
    <Programm/>
    <Tariffs/>
    <Faq/>
    <TheFooter/>
  </div>
</template>

<style lang="sass">
@import "vars.sass"

@font-face
  font-style: regular
  font-weight: 400
  font-display: swap
  font-family: "RobotoCondensed"
  src: local("RobotoCondensed-Regular")
  src: url("assets/fonts/RobotoCondensed-Regular.woff2") format("woff2")
  src: url("assets/fonts/RobotoCondensed-Regular.woff") format("woff")
  src: url("assets/fonts/RobotoCondensed-Regular.ttf") format("ttf")

/*#scrollbar*/
::-webkit-scrollbar-track
  background-color: $white

::-webkit-scrollbar-thumb
  background-color: $violet
  border-radius: 0.5rem

::-webkit-scrollbar-thumb:active
  background-color: $violet-light

::-webkit-scrollbar
  width: 0.6rem

/*#common*/
html
  font: 400 14px /1.2 'RobotoCondensed', sans-serif
  text-transform: uppercase

body
  scroll-behavior: smooth

h2
  font-size: 3.57rem
  line-height: 1.18
  margin-bottom: 0.6rem

.wrapper
  overflow-x: hidden

.container
  display: flex
  padding: 0 2rem
  margin: 0 auto
  box-sizing: content-box
  max-width: 83.5rem
  justify-content: space-between
  align-items: center
  flex-direction: column
  gap: 4.3rem

footer
  background: rgba(37, 25, 51, 1)

section:nth-child(odd)
  padding-top: 12rem
  background: $white
  color: $violet

section:nth-child(even)
  background: $violet
  color: $white
  padding: 12rem 0 10.6rem

section.promo
  padding: 0
  padding-bottom: 8rem
  background: #4c3d74

section:not(.promo), .footer
  opacity: 0
  transition: opacity 1s ease-in-out

section.fade-in, .footer.fade-in
  opacity: 1

.logo
  height: 6em
  padding: 1.5em
  will-change: filter
  transition: filter 300ms

a
  color: white

a:hover
  transform: scale(1.08)
  text-decoration: underline
  transition: all 0.3s ease-out

.footer__list:not(:first-child) .link:hover
  text-decoration: none

footer a
  line-height: 1.5

.footer .txt
  color: $white

.types__title
  margin-right: 15%

.faq__title, .programm__title
  margin-left: 5%
  align-self: flex-start

.faq__container
  gap: 4rem

@media screen and (max-width: 912px)

  .title
    margin-right: 0
    margin-bottom: 0
    text-align: center

  section:nth-child(even)
    padding-bottom: 8rem
    padding-top: 8rem

  section:nth-child(odd)
    padding-top: 8rem

@media screen and (max-width: 767px)

  .title
    font-size: 2.86rem

  .container
    padding: 0 1.5rem

  .faq__container
    gap: 6rem

@media screen and (max-width: 480px)

  section:nth-child(even)
    padding-bottom: 6rem
    padding-top: 6rem

  section:nth-child(odd)
    padding-top: 6rem

  .container
    padding: 0 1rem

  .title
    font-size: 2.14rem

@media screen and (max-width: 360px)

  .faq__container
    gap: 4rem

  .title
    font-size: 1.8rem

</style>
