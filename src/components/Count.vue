<template>
  <div>
    <div>this is Count</div>
    <div>{{obj.b}}</div>
  </div>
</template>
<script>
import _ from 'lodash'
export default {
  name: 'Count',
  data() {
    return {
      obj: {
        a: 'a',
        b: 'b'
      }
    }
  },
  mounted() {
    this.obj = _.omit(this.obj, 'a')
    console.log('this.obj', this.obj)
  }
}

</script>
