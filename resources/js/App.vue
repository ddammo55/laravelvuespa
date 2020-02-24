<template>
  <main>
    <Header></Header>

    <div id="layoutSidenav">
        <Sidebar/>
      <div id="layoutSidenav_content">
        <main>
            <router-view></router-view>
        </main>



        <Footer/>
      </div>
    </div>
  </main>
</template>

<script>
    import Header from './components/Header.vue';
    import Sidebar from './components/Siderbar.vue';
    import Footer from './components/Footer.vue';

    export default {
        components:{
          Header,
          Sidebar,
          Footer
        }
    }
</script>

