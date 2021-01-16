<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/> -->
     <el-select v-model="value" placeholder="请选择">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value">
    </el-option>
  </el-select>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        options: [{
          value: '选项1',
          label: '+'
        }, {
          value: '选项2',
          label: '-'
        }, {
          value: '选项3',
          label: '*'
        }, {
          value: '选项4',
          label: '/'
        }, {
          value: '选项5',
          label: ''
        }],
        value: ''
      }
    }
  }
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
