<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <p>
        If Element is successfully added to this project, you'll see an
        <code v-text="'<el-button>'"></code>
        below
      </p>
      <el-button>el-button</el-button>
    </div>
    <el-main>
      <el-row type="flex" justify="center">
        <el-col :span=16>
          <ListItem :items="[{name: 'Netflix', price: 10.99, interval: 'monthly'}, {name: 'VPN Express', price: 12.00, interval: 'monthly'}]" />
        </el-col>
      </el-row>
    </el-main>
  </div>
</template>

<script>
import ListItem from './components/ItemList.vue'

export default {
  name: 'app',
  components: {
    ListItem
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
