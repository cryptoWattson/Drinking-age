<template>
  <div>
    <h1>Hello World</h1>
    <counter
    : year ="2020"
    :month-"4"
    :date-"1"
    :hour-"14"
    :minute-"23"
    :second-"59"
    :millisecond-"59"
    />
  </div>
</template>

<script>
const { default: counter }=require("@/components/counter.vue")

export defa
  components: { counter },ult {

};
</script>

<style scoped>

</style>