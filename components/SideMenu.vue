<template>
  <div>
    <b-button v-b-toggle.sidebar-1>Toggle Sidebar</b-button>
    <b-sidebar id="sidebar-1" title="Sidebar" shadow>
      <div class="px-3 py-2">
        <nav>
        <b-nav-items href="#">
          <div class="icon">
            <b-icon icon="house-door-fill" class="menu"></b-icon><label>Home</label>
          </div>
        </b-nav-items>
        <b-nav-items href="#">
          <div class="icon">
            <b-icon icon="bar-chart-fill" class="menu"></b-icon><label>Menu</label>
          </div>
        </b-nav-items>
        <b-nav-items href="#">
          <div class="icon">
            <b-icon icon="gift" class="menu"></b-icon><label>Box</label>
          </div>
        </b-nav-items>
        <b-nav-items href="#">
          <div class="icon">
            <b-icon icon="layout-text-sidebar" class="menu"></b-icon><label>Chat</label>
          </div>
        </b-nav-items>
        <b-nav-items href="#">
          <div class="icon">
            <b-icon icon="gear" class="menu"></b-icon><label>Settings</label>
          </div>
        </b-nav-items>
        <b-nav-items href="#">
          <div class="icon">
            <b-icon icon="person" class="menu"></b-icon><label>Person</label>
          </div>
        </b-nav-items>
      </nav>
      </div>
    </b-sidebar>
  </div>
</template>
<script>
export default {
    name:'side-bar'
}
</script>
<style scoped>
.btn-secondary {
    color: #fff;
     background-color: transparent; 
    border-color: #6c757d;
}
.icon{
  color: rgb(27, 27, 73);
  padding-bottom:10px;
}
label {
    display: inline-block;
    margin-bottom: 0.5rem;
    margin-left: 20px;
     color: rgb(27, 27, 73);
}
.menu{
  font-size: 1.3rem;
}
.b-sidebar {
    display: flex;
    flex-direction: column;
    position: fixed;
    top: 0;
    width: 220px !important;
    max-width: 100%;
    height: 100vh;
    max-height: 100%;
    margin: 0;
    outline: 0;
    transform: translateX(0);
}
</style>