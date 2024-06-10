<script>
import Img from './Img.vue';
import HeaderList from './HeaderList.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button, HeaderList },
  props: ['tariff','tariffsImg'],
}
</script>
<template>
    <div>
        <Img :src="tariffsImg"/>
        <h3>LITE (САМОСТОЯТЕЛЬНЫЙ)</h3>
        <HeaderList :litem="tariff" />
        <div>
            <div>ДЛИТЕЛЬНОСТЬ: 14 ДНЕЙ</div>
            <div>
                <div>КАЖДЫ2 20 ОПЛАТ + 1111 Р.</div>
                <div>6666 Р.</div>
            </div>
        </div>
        <Button/>
    </div>
</template>
<style scoped lang="sass">
@import "../vars.sass"
</style>