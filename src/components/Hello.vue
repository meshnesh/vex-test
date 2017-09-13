<template>
  <div class="container">
    <div class="row text-center">
      <h3>
        Clicked : {{ $store.state.count }} times, counter is {{ evenOrOdd }}
      </h3>
      <button class="btn btn-success" @click="increment">+</button>
      <button class="btn btn-danger" @click="decrement">-</button>

      <button class="btn" @click="incrementIfOdd"> increment if odd </button>
      <button class="btn" @click="incrementAsync"> increment async </button>
    </div>
  </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
  name: 'hello',
  computed: mapGetters([
    'evenOrOdd'
  ]),
  methods: mapActions([
    'increment',
    'decrement',
    'incrementIfOdd',
    'incrementAsync'
  ])
}
</script>

