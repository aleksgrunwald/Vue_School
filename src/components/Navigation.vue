<template>
  <div>
    <nav>
      <router-link class="spacing" v-for="routes in links" 
      v-bind:key="routes.id"
      :to="`${routes.page}`">{{routes.text}}</router-link>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navigation',
  data() {
    return {
      links: [
        {
          id: 0,
          text: 'Classroom 1',
          page:'/classroom1'
        }
      ]
    }
  }
}
</script>

<style scoped>
nav {
  background: #2b1563;
  height: 6%;
  width: 100%;
  position: fixed;
  top: 0;
}
.spacing {
  margin-right: 10px;
  color: white;
  text-decoration: none;
}
</style>