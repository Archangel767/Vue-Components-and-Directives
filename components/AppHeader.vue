<template>
  <header class="header">
    <h1 class="title">cpnt200-a4</h1>
    <ul>
      <li>
        <nuxt-link to='/'>Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to='/gallery'>Gallery</nuxt-link>
      </li>
      <li>
        <nuxt-link to='/todo'>To Do</nuxt-link>
      </li>
      <li>
        <nuxt-link to='/about'>About</nuxt-link>
      </li>
    </ul>  
          
  </header>  
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

<style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items:center;
    margin-bottom: 1rem;
    padding-bottom: 1rem;
    border-bottom: 1px dotted grey;
} 

  .header .title {
  font-size: 3rem;
  color: #526488;
}

  .header ul {
    display: flex;
}

  .header a {
    display: inline-block;
    background: #333;
    color: white;
    padding: 0.3rem 1rem;
    margin-right: 0.5rem;
}
</style>