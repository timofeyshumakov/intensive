<script>
import Img from './Img.vue';
  export default {
    components: { Img },
    props: {
        card: Object
    }
  }
</script>
<template>
    <div class="card">
        <Img class="img" :src="`${card.img.src}`" alt="Image of a cat" />
        <div class="txt">{{ card.txt }}</div>
    </div>
</template>
<style scoped lang="sass">
@import "../vars.sass"

</style>