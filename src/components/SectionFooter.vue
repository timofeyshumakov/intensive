<script>
import Img from './Img.vue';
import Button from './Button.vue';
export default {
  components: { Img, Button },
  props: ['sectionName', 'img', 'button', 'txt', 'social', 'prize', 'hashtag'],
}
</script>
<template>
    <div>
    <div v-if="sectionName === 'programm'">

    </div>
    <div v-if="sectionName === 'types'">
        <Img v-if="sectionName === 'faq'" class="social" src="common/telegramm.svg" alt="Image of a cat" />
        <div>{{ txt }}</div>
        <Button v-if="sectionName !== 'faq' && sectionName !== 'tariffs'" class="button primary-button" link="#1" txt="ЗАПИСАТЬСЯ"/>
        <Button v-else-if="sectionName !== 'faq'" class="button primary-button" link="#1" txt="НАПИСАТЬ"/>
        <Button v-else-if="sectionName !== 'tariffs'" class="button primary-button" link="#1" txt="СТОРИС-ШАБЛОН"/>
        <Img class="main-img" src="common/woman-supervillain.svg" alt="Image of a cat" />
    </div>
    </div>
</template>
<style lang="sass">

</style>