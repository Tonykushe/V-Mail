<template>
  <div id="app">
    <div class="container">
      <div class="mail-box">
        <app-sidebar></app-sidebar>
        <app-content></app-content>
      </div>
    </div>
  </div>
</template>

<script>
import SideBar from './components/SideBar'
import Content from './components/Content'

export default {
  name: 'app',
  components: {
    appSidebar: SideBar,
    appContent: Content
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
