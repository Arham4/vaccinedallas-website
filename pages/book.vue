<template>
  <div>
    <LocationSelector />
  </div>
</template>

<script>
export default {
  components: {
    LocationSelector: () => import('@/components/LocationSelector')
  }
}
</script>
