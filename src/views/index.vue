<template>
  <div class="about">
    <h1>index page</h1>
    <p>ここで動作確認</p>
    <Sticky />
    <Sticky />
  </div>
</template>

<script>
import Sticky from '@/components/sticky.vue'
export default {
  name: 'index',
  components: {
    Sticky
  }
}
</script>