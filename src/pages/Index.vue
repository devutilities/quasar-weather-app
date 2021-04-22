<template>
  <q-page class="flex flex-center">
    <img
      v-for="item in contador"
      :key="item"
      alt="Quasar logo"
      src="~assets/quasar-logo-full.svg"
      @click="clique"
    />
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      contador: 1,
      i: 0
    }
  },
  methods: {
    clique () {
      alert('teste')
    }
  }
}
</script>
