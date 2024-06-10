<script>
import HeaderList from './HeaderList.vue';
import Img from './Img.vue';
const format ="svg";
const sectionName = "programm";
export default {
  components: { HeaderList, Img },
  data() {
    return {
        sectionName,
        markSheme: " +",
        litem: [
            {txt: "ВВОДНЫЙ УРОК"},
            {txt: "СКОРОСТНОЕ СНЯТИЕ РЕСНИЦ"},
            {txt: "РАБОТА С КЛЕЕМ. КАК ПРОДЛИТЬ НОСКУ"},
            {txt: "ЗДОРОВЬЕ МАСТЕРА"},
            {txt: "ЛИЧНЫЙ БРЕНД В INSTAGRAM: ПОЧЕМУ УВЯДАЮТ КОММЕРЧЕСКИЕ АККАУНТЫ"},
            {txt: "ЛОМАЕМ СТЕРЕОТИПЫ МОДЕЛИРОВАНИЯ: ЧЕМ СЛОЖНЕЕ ПРИДУМАЛ, ТЕМ СЛОЖНЕЕ ЖИТЬ"},
            {txt: "КЛАССИЧЕСКОЕ НАРАЩИВАНИЕ РЕСНИЦ"},
            {txt: "ПУЧОК. КАК БЫСТРО И ПРАВИЛЬНО ФОРМИРОВАТЬ ТЕБЯ, ДРУЖОК?"},
            {txt: "НАРАЩИВАЕМ ОБЪЕМЫ 2D+ "}
        ],
    }
    }
}
</script>
<template>
    <section :class="sectionName">
        <div class="container">
            <h2>ВОТ ТАКАЯ ПРОГРАММА ИНТЕНСИВА</h2>
            <HeaderList :litem="litem" :markSheme="markSheme" :sectionName="sectionName"/>
        </div>
    </section>
</template>
<style scoped lang="sass">

</style>