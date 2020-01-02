<template>
  <header class="global-navigation">
    <nav class="global-navigation__menu">
      <ul>
        <li v-for="item in navItems" :key="item.text">
          <nuxt-link :to="item.path">{{ item.text }}</nuxt-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      navItems: [
        { path: '/', text: 'Home' },
        { path: '/about', text: 'About' },
        { path: '/resume', text: 'Resume' },
        { path: '/portfolio', text: 'Portfolio' },
        { path: '/contact', text: 'Contact' }
      ]
    }
  }
}
</script>

<style scoped>
.global-navigation {
  height: 80px;
  background-color: #bbc2e2;
}
ul {
  padding: 0;
  margin: 0;
  list-style-type: none;
}
ul > li {
  display: inline-block;
  padding: 15px;
}
a {
  color: #6665dd;
  text-decoration: none;
  font-size: 18px;
  text-transform: capitalize;
}
</style>
