<script>
import Img from './Img.vue';
import HeaderList from './HeaderList.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button, HeaderList },
  props: ['tariff', 'tariffsImg', 'sectionName', 'tariffsIndex'],
}
</script>
<template>
    <div class="tariff">
        <Img class="tariff-img" :src="tariffsImg"/>
        <h3 class="title">LITE (САМОСТОЯТЕЛЬНЫЙ)</h3>
        <HeaderList :litem="tariff" :sectionName="sectionName" :tariffsIndex="tariffsIndex"/>
        <div class="tariff-footer">
            <div>ДЛИТЕЛЬНОСТЬ: 14 ДНЕЙ</div>
            <div class="tariff-footer-bottom">
                <div class="tariff-info">КАЖДЫ2 20 ОПЛАТ + 1111 Р.</div>
                <div>6666 Р.</div>
            </div>
        </div>
        <Button class="tariff-button button primary-button" link="#" txt="ОПЛАТИТЬ"/>
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
</style>