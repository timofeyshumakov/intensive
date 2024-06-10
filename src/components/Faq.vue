<script>
import HeaderList from './HeaderList.vue';
const sectionName = "faq";
export default {
  components: { HeaderList },
  data() {
    return {
        sectionName,
        litem: [
            {txt: "Я ТОЧНО ВСЕМУ НАУЧУСЬ? У МЕНЯ ПОЛУЧИТСЯ?"},
            {txt: "КАК Я БУДУ УЧИТЬСЯ СКОРОСТНОМУ НАРАЩИВАНИЮ ОНЛАЙН?"},
            {txt: "СКОЛЬКО ВРЕМЕНИ БУДЕТ УХОДИТЬ НА ВЫПОЛНЕНИЕ ДЗ?"},
            {txt: "КАК ЧАСТО БУДУТ ВЫХОДИТЬ УРОКИ?"},
            {txt: "КАКАЯ ТЕХНИКА БУДЕТ ОТРАБАТЫВАТЬСЯ: РУЧНАЯ ИЛИ ЛЕНТОЧНАЯ?"}
        ],
    }
    }
}

</script>
<template>
    <section :class="sectionName">
        <div class="container">
            <h2>А ТАКИЕ ВОПРОСЫ МОГУТ БЫТЬ У ВАС</h2>
            <HeaderList :litem="litem" :sectionName="sectionName"/>
        </div>
    </section>
</template>
<style scoped lang="sass">

</style>