<template>
  <div id="app">
    <v-app>
      <v-toolbar app dark class="nav_grey" height="70px">
        <v-toolbar-items>
          <img src="static/images/logo.png" alt="edu.pro" class="logo" />
        </v-toolbar-items>
        <v-toolbar-title>
            <span class="name_first">edu.</span><span class="name_last">pro</span>
        </v-toolbar-title>
        <v-spacer></v-spacer>
          <v-btn icon >
            <v-icon dark>search</v-icon>
          </v-btn>
          <v-btn icon to="/Login">
            <v-icon dark >apps</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon dark>close</v-icon>
          </v-btn>
      </v-toolbar>
      <v-content>

          <router-view></router-view>

      </v-content>
      <v-footer class="pa-3">
        <v-spacer></v-spacer>
        <div>&copy; {{ new Date().getFullYear() }}</div>
      </v-footer>
    </v-app>
  </div>
</template>

<script>
  export default {
    name: 'App',
    data: () => ({
      title: 'edu.pro client',
      menu_items: [
        { title: 'Home', icon: 'dashboard' },
        { title: 'About', icon: 'question_answer' }
      ],
    })
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons');
  /* Global CSS */
  .logo {
    width: auto;
    height: 40px;
    margin: auto;
  }

  .nav_grey {
    background-color: #5b5b5b!important;
  }

  .name_first {
    color: white;
    font-weight: 300;
    font-size: 24px;
  }

  .name_last {
    color: #ee8c88;
    font-weight: 500;
    font-size: 24px;
  }
</style>
