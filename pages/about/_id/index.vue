<template>
  <p>About Page số {{ id }}</p>
</template>

<script>
export default {
  validate({ params }) {
    return /^\d+$/.test(params.id)
  },
  asyncData({ params }) {
    // eslint-disable-next-line no-console
    console.log('params', params)
    return {
      id: params.id,
    }
  },
}
</script>
