<template>
  <div class="home">
    <list />
  </div>
</template>

<script>
// @ is an alias to /src
import list from '@/components/list.vue'


export default {
  name: 'home',
  components: {
    list
  }
}
</script>
