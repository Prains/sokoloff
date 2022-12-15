<template>
  <Header />
  <Main />
  <Advantage />
  <Catalog />
  <Contacts />
</template>

<script>
import Advantage from './components/Advantage.vue'
import Catalog from './components/Catalog.vue'
import Contacts from './components/Contacts.vue'
import Header from './components/Header.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Advantage,
    Catalog,
    Contacts
  }
}
</script>

<style>
@import url('./styles/normalize.css');
@import url('https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

* {
  box-sizing: border-box;
}

a {
  color: unset;
  text-decoration: none;
}

p {
  margin: 0
}


#app {
  font-family: 'Crimson Pro', serif;

}
</style>
