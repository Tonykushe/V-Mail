<template>
  <div id="app">
    <div class="container">
      <div class="mail-box">
        <SideBar/>
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from './components/SideBar'

export default {
  name: 'app',
  components: {
    SideBar
  }
}
</script>

<style>
.mail-box {
    border-collapse: collapse;
    border-spacing: 0;
    display: table;
    table-layout: fixed;
    width: 100%;
}

</style>
