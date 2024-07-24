<script>
const sectionName = "footer";
import HeaderList from './HeaderList.vue'
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
  components: { HeaderList },
  data() {
    return {
      sectionName,
      items: [
        [
          {txt: "ЮЛИЯ ВОРМАН"},
          {txt: "ИНН:"},
          {txt: "ОГРНИП:"}
        ],
        [
          {txt: "НАВЕРХ", link: "#"},
          {txt: "Design by @kemfetka", link: "#"}
        ],
        [
          {txt: "ПОЛИТИКА КОНФИДЕНЦИАЛЬНОСТИ", link: "#"},
          {txt: "ДОГОВОР-ОФЕРТА", link: "#"},
          {txt: "СВЯЗАТЬСЯ С НАМИ", link: "#"}
        ]
      ]
  }
}
};
</script>

<template>
    <footer class="footer" ref="sectionRef">
        <div class="container">
          <HeaderList v-for="item in items" :litem="item" :sectionName="sectionName"/>
        </div>
    </footer>
</template>



<style scoped lang="sass">
@import "../vars.sass"

.footer
  padding: 9rem 0
  background: #251933

.container
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

@media screen and (max-width: 767px)

  .footer__item
    justify-content: flex-start

  .container
    gap: 0.75rem

  .footer
    padding: 6rem 3rem 6rem 3rem 

  .container
    grid-template-columns: 1fr

@media screen and (max-width: 360px)

  .footer
    padding: 4rem 1rem 4rem 1rem 

</style>