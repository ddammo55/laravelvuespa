<template>
  <div id="layoutSidenav_nav">
    <nav class="sb-sidenav accordion sb-sidenav-dark" id="sidenavAccordion">
      <div class="sb-sidenav-menu">
        <div class="nav">
          <div class="sb-sidenav-menu-heading">Core</div>

          <router-link to="/" class="nav-link" exact>
            <i class="fas fa-tachometer-alt"></i>
            <span>Dashboard</span>
          </router-link>

          <div class="sb-sidenav-menu-heading">Interface</div>

          <router-link to="/categories" class="nav-link" exact>
            <i class="fas fa-fw fa-chart-area"></i>
            <span>Categories</span>
          </router-link>


        </div>
      </div>
      <div class="sb-sidenav-footer">
        <div class="small">Logged in as:</div>Start Bootstrap
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>
