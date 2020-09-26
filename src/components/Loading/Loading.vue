<template>
  <div
    class="vue-loading"
    :style="loadingStyle"
    v-html="svg"
  >
  </div>
</template>
<script>
const StyleLoading = require('./svg')
export default {
  name: 'vueLoading',
  props: {
    type: {
      type: String,
      default: 'bead'
    },
    color: {
      type: String,
      default: 'yellow'
    },
    size: { width: '30px', height: '30px' }
  },
  data() {
    return {};
  },
  computed: {
    loadingStyle: function() {
      return {
      fill: this.color,
      width: this.size.width,
      height: this.size.height
      }
    },
    svg: function () {
      return StyleLoading[this.type];
    }
  },
  created() {}
};
</script>

<style>
.vue-loading {
  margin: auto;
}
</style>





