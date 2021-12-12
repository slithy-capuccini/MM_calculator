
<template>
  <div>
    <h3 class="center">{{ msg }}</h3>
    <TableElements />
  </div>
</template>

<script>
import TableElements from './element.vue'

export default {
  name: 'HelloWorld',
  components: {
    TableElements
  },
  props:{
    msg:Text,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.no-row {
  border:none;
}
.nometales{
  background-color: #A2F0F1;
}
.alcalino{
  background-color: #e78463;
}
.alcalinoterreo{
  background-color: #be9f4f;
}
.inerte{
  background-color:#a97bca;
}
.metal-trans{
  background-color:#95E28C;
}
.metales{
  background-color:#8C8C8C;
}
.metaloides{
  background-color:#6C99E3;
}
.halogenos{
  background-color:#e98dc4;
}
h3 {
  font-size: 18px;
}
h4{
  font-size: 12px;
}
</style>
        