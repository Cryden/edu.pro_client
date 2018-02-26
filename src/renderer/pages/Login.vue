<template>
  <v-container fill-height>
    <v-layout wrap align-center>
      <v-flex xs12 sm4 offset-sm4 class="text-xs-center">
        <div class="subheading mb-3 primary--text">Пожалуйста авторизуйтесь</div>
        <v-form>
            <v-text-field
            label="Имя пользователя"
            hide-details
            class="mb-3"
            ></v-text-field>
            <v-text-field
            label="Пароль"
            :append-icon="e1 ? 'visibility' : 'visibility_off'"
            :append-icon-cb="() => (e1 = !e1)"
            :type="e1 ? 'password' : 'text'"
            class="mb-3"
            ></v-text-field>         
            <v-btn flat depressed class="ma-0 primary--text"><v-icon left >check_circle</v-icon>Вход</v-btn>
        </v-form>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
    data () {
      return {
        e1: false
      }
    }
  }  
</script>

<style>
.primary--text {
    color: #b4b4b4!important;
}

</style>
