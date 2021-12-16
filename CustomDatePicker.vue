<template>
  <el-date-picker
    v-model="value"
    v-bind="$attrs"
    @change="handleChange"
    v-on="$listeners"
    >
  </el-date-picker>
</template>

<script>
export default {
  name: '',
  props: {
    begin:{
      type: [String, Number, Object, Date],
      default: ''
    },
    end:{
      type: [String, Number, Object, Date],
      default: ''
    },
  },
  data(){
    return {
      value: []
    }
  },
  methods: {
    handleChange(){
      this.$emit('update:begin', this.value && this.value[0])
      this.$emit('update:end', this.value && this.value[1])
    }
  }
}
</script>

<style>

</style>