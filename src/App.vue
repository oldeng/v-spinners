<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">预览</router-link> |
      <router-link to="/experiment">实验</router-link> |
      <router-link to="/docs">文档</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style lang="less">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #ffffff;
    background: radial-gradient(ellipse at center, #0a2e38 0%, #000000 70%);
    background-repeat: none;
    background-size: 100% 100%;
    position: absolute;
    left: 0;
    top: 0;
    right: 0;
    bottom: 0;
}

#nav {
  padding: 15px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
