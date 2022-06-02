<template>
    <Date @handleChange="payload => active = payload" />
    <Time :date="active" />
</template>


<script>
import Date from './Date.vue'
import Time from './Time.vue'
import AutoImport from 'unplugin-auto-import/vite'
import Components from 'unplugin-vue-components/vite'
import { ElementPlusResolver } from 'unplugin-vue-components/resolvers'


export default {
  components: {
    Date,
    Time,
  },
  data() {
    return {
      active: null
    }
  },
  plugins: [
    // ...
    AutoImport({
      resolvers: [ElementPlusResolver()],
    }),
    Components({
      resolvers: [ElementPlusResolver()],
    }),
  ],
}
</script>