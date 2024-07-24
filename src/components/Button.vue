<script>
export default {
  props: ['link', 'txt', 'buttonClassName', 'formClassName']
}
</script>
<template>
    <form :class="formClassName" :action="link">
        <button :class="buttonClassName">{{ txt }}</button>
    </form>
</template>
<style lang="sass">

@import "../vars.sass"


.button
    border-radius: 2rem
    min-width: 17.5rem
    min-height: 4.3rem
    color: white
    font-size: 1.15rem
    width: fit-content
    height: fit-content
    display: flex
    justify-content: center
    align-items: center

.button:hover
    transform: scale(1.04)

.primary-button:hover
    background: $violet-light-hover

.secondary-button:hover
    background: #4b3b77

.primary-button
    background: $violet-light

.secondary-button
    background: $violet
    border: 3px solid $violet-light
    
.primary-button button
    background: $violet-light

.tariff-button
    position: absolute

</style>