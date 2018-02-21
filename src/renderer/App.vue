<template>
  <div id="app">
    <v-app>
      <v-toolbar app>
        <v-toolbar-items>
          <img src="/static/logo.png" alt="EDU.pro" class="logo" />
        </v-toolbar-items>
        <v-toolbar-title>EDU.pro</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn flat v-for="item in menu_items" :key="item.title">
            <v-icon left>{{ item.icon }}</v-icon>
            {{ item.title }}
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
      <v-content>
        <v-container fluid>
          <router-view></router-view>
        </v-container>
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
    height: 50px;
    margin-top: 8px;
  }
</style>
