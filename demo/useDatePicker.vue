<template>
  <custom-date-picker
    :begin.sync="effectStartTime"
    :end.sync="effectEndTime"
    value-format="timestamp"
    type="datetimerange"
    range-separator="至"
    start-placeholder="开始日期"
    end-placeholder="结束日期"
    @change="handleChange"/>
</template>

<script>
export default {
  data(){
    return {
      effectStartTime: '',
      effectEndTime: ''
    }
  }
}
</script>

<style>

</style>