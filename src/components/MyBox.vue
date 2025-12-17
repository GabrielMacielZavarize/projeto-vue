<template>
  <div class="box">
    {{name}} - {{age}} - {{description}}
    <span :class="['status', status]"> - {{status}}</span>
  </div>
</template>

<script>
export default {
  name: 'MyBox',
  props: {
    name: {
      type: String,
      default: "N/A"
    },
    age:{
      type: Number,
      required: true
    },
    description:{
      type: String,
      default: "Sem Descrição"
    },
    status:{
      type: String,
      validator: value => ['active', 'inactive'].includes(value),
      default: 'ativo'
    }
  }
}
</script>

<style>
.box {
  min-width: 30px;
  min-height: 30px;
  background-color: antiquewhite;
  align-items: center;
  justify-content: center;
  display: flex;
}
.active {
  background-color: green;
}
.inactive {
  background-color: red;
}
</style>