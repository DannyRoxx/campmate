<template>
  <div class="home">
    <h1>CAMP MATE</h1>
    
    <div class="preset-menu">
        <p>Presets (pil ned)</p>
        <ul class="presets">
            <li class="preset" @click="addPreset1()">Camping</li>
            <li class="preset" @click="addPreset2()">Festival</li>
            <li class="preset" @click="addPreset3()">Travel</li>
        </ul>
    </div>

    <list />
  </div>
</template>

<script>
// @ is an alias to /src
import topbob from '@/components/topbob.vue'
import list from '@/components/list.vue'
import presets from '@/components/presets.vue'
import {
  db
} from '../firebaseConfig'


export default {
  name: 'home',
  components: {
    topbob,
    list,
    presets
  },
  methods: {
    addPresent1() {
      
    }
  }
}
</script>

<style>
  h1 {
    font-size: 3rem;
    padding: 1rem;
    margin: 0;
    color: #ffffff;
    background-color: black;
  }

  .preset-menu {
    margin: 1% 25%;
    text-align: left;
  }

  .presets {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 1%;
    text-align: center;
  }

  .preset {
    background-color: red;
    padding: 2%;
    cursor: pointer;
  }
</style>
