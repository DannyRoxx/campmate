<template>
        <ul class="presets">
            <li class="preset" @click="addPreset1()">Camping</li>
            <li class="preset" @click="addPreset2()">Festival</li>
            <li class="preset" @click="addPreset3()">Travel</li>
        </ul>
</template>

<script>
import { bus } from '@/main.js'

export default {
    name: 'preset-list',
  data() {
    return {
      camping: ['ting1', 'ting2', 'ting3', 'ting4'],
      festival: ['ting5', 'ting6', 'ting7', 'ting8'],
      travel: ['ting9', 'ting10', 'ting11', 'ting12']
    }
  },
  methods: {
    addPreset1() {
      bus.$emit('create-camping', this.camping)
      this.camping.push()
    },
    addPreset2() {
      bus.$emit('create-festival', this.festival)
      this.festival.push()
    },
    addPreset3() {
      bus.$emit('create-travel', this.travel)
      this.travel.push()
    }
  }
}
</script>

<style>

</style>