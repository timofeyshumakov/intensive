<script>
export default {
  props: ['link', 'txt', 'class']
}
</script>
<template>
    <form :action="link">
        <button :class="class">{{ txt }}</button>
    </form>
</template>
<style lang="sass">
@import "../vars.sass"
.button
    background: $violet
    border-radius: 2rem
    min-width: 17.5rem
    min-height: 4.3rem
    color: white
    font-size: 1.15rem

.primary-button
    background: $violet-light

.secondary-button
    background: $violet
    border: 3px solid $violet-light
    
</style>