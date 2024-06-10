<template>
    <ul class="list">
        <li class = "item" v-for="(item, index) in litem">
          <Img v-if="item.src !==undefined" class="img" :src="item.src" alt="Image of a cat" />
          <a v-if="item.link !== '' && item.link !== undefined"  :href="`${item.link}`" class = "link">{{ item.txt }}</a>
          <span v-else-if="sectionName === 'programm'">УРОК {{ index + 1}}. {{ item.txt }}</span>
          <span v-else>{{ item.txt }}</span>
          <span v-if="sectionName === 'programm'"><span>+</span></span>
          <span v-if="sectionName === 'tariffs' && mark === '-'">-</span>
          <span v-else-if ="sectionName === 'tariffs'">+</span>
          <span v-if="item.title !==undefined">{{ item.title }}</span>
          <span v-if="sectionName === 'faq'">+</span>
        </li>
    </ul>
</template>
<script>
import Img from './Img.vue';
  export default {
    components: { Img },
    props: {
      litem: Object,
      markSheme: String,
      sectionName: String
    }
  }
</script>
<style lang="sass">



</style>