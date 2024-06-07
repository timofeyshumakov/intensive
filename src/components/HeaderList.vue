<template>
    <ul class="list">
        <li class = "item" v-for="(item) in litem">
          <a v-if="item.link !== '' && item.link !== undefined"  :href="`${item.link}`" class = "link">{{ item.txt }}</a>
          <span v-else>{{ item.txt }}</span>
        </li>
    </ul>
</template>
<script>
  export default {
    props: {
      litem: Array,
      className: String
    }
  }
</script>
<style lang="sass">



</style>