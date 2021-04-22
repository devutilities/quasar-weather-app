<template>
  <q-page class="flex flex-center">
    <p class="text-h2">Login</p>
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
