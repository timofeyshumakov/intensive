<script>
import Img from './Img.vue';
import HeaderList from './HeaderList.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button, HeaderList },
  props: ['tariff', 'tariffsTitle', 'tariffsImg', 'sectionName', 'tariffsIndex', 'tariffsPrice'],
}
</script>
<template>
    <div class="tariff">
        <Img class="tariff-img" :src="tariffsImg" alt=" "/>
        <h3 class="title">{{ tariffsTitle }}</h3>
        <HeaderList :litem="tariff" :sectionName="sectionName" :tariffsIndex="tariffsIndex"/>
        <div class="tariff-footer">
            <div>ДЛИТЕЛЬНОСТЬ: 14 ДНЕЙ</div>
            <div class="tariff-footer-bottom">
                <div class="tariff-info">КАЖДЫ2 20 ОПЛАТ + 1111 Р.</div>
                <div>{{ tariffsPrice }} Р.</div>
            </div>
        </div>
        <Button formClassName="tariff__form" buttonClassName="tariff-button button primary-button" link="#" txt="ОПЛАТИТЬ"/>
    </div>
</template>
<style scoped lang="sass">
@import "../vars.sass"

.tariff
    background: #F2EEF7
    color: $violet
    padding: 2rem
    border-radius: 2rem
    position: relative
    max-width: 25.5rem
    display: flex
    flex-direction: column
    gap: 1.5rem

.tariff-footer
    font-size: 1.15rem
    display: flex
    flex-direction: column
    gap: 1rem

.tariff-footer-bottom
    display: flex
    justify-content: space-between

.tariff-info
    font-size: 0.9rem

.title
    font-size: 1.15rem
    text-align: start

.tariff__form
    width: 100%
    display: flex
    align-items: flex-start
    justify-content: center
    
</style>