<template>
  <div id="app">
    <Element/>
    <List/>
  </div>
</template>

<script>
import Element from './components/Header.vue'
import List from './components/List.vue'
//import Detail from './components/Detail.vue'

export default {
  name: 'App',
  components: {
    List,
    Element
    //Detail
  }
}
</script>

