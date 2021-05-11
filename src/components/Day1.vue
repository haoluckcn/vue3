<template>
  <h1>{{ title }}</h1>
  <p>支持人数：{{zc}}</p>
  <p>反对人数：{{fd}}</p>
  <p>支持率：{{zcl}}</p>
  <button @click="change('zc')">支持</button>
  <button @click="change('fd')">反对</button>
</template>

<script>
import { reactive, toRefs, computed } from 'vue'
export default {
  props: {
    title: {
      type: String,
      default: () => ''
    }
  },
  setup(){
    const state = reactive({
      zc: 0,
      fd: 0
    })
    const change = (type) => {
      type === 'zc' ? state.zc++ : state.fd++
    }
    const zcl = computed(() => {
      let count = state.zc + state.fd
      count ? count = (state.zc / count * 100).toFixed(2) : null
      return `${count}%`
    })
    return {
      ...toRefs(state),
      zcl,
      change
    }
  }
}
</script>
