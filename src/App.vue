<template>
  <div id="app">

    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.card-header:first-child {
    border-radius: calc(.25rem - 1px) calc(.25rem - 1px) 0 0;
    height: 50px;
}
.card-header {
    padding: .75rem 1.25rem;
    margin-bottom: 0;
    background-color: #363636;
    border-bottom: 1px solid rgba(0,0,0,.125);
}
.card-header-title {
    align-items: center;
    color: #363636;
    display: flex;
    flex-grow: 1;
    font-weight: 700;
    padding: .75rem 1rem;
}

.section {
    padding: 2rem 1.5rem;
}
</style>
