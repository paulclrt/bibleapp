<template>
    <div id="nav" class="d-flex flex flex-row justify-between align-middle">
        <Dmenu :class="{ 'basis-1/3':true, 'justify-start':true }"/>
        <h1 id="maintitle" class="text-xl font-bold leading-none tracking-tight text-gray-900 md:text-2xl lg:text-3xl text-center py-auto basis-1/3">
            {{ maintitle }}
        </h1>
        
        <div id="rightslots" class="basis-1/3">
            <slot></slot>
        </div>
    </div>
</template>




<script>
import Dmenu from "./dropdown.vue"

export default {
  name: 'main',
  components: {
      Dmenu,
  },
  props: ["maintitle"],
  data: function() {
      return {
      }
  },
  methods: {
  }
}
</script>

<style scoped>
div.nav {
    height: 10vh;
}
</style>
