<template>
  <div class="hello">
    Counter : {{ $store.state.count }}, counter is {{ evenOrOdd }}
  </div>
</template>

<script>
import {mapGetters} from 'vuex'
export default {
  name: 'hello',
  computed: mapGetters([
    'evenOrOdd'
  ])
}
</script>

