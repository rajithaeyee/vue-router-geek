<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="ts">

export default {
  name: 'about',
  components: {
  },
  
  beforeRouteLeave (to:any, from:any, next:any) {
  const answer = window.confirm('Do you really want to leave? you have unsaved changes!')
  if (answer) {
    next()
  } else {
    next(false)
  }
}
}
</script>