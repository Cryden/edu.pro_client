<template>
  <div>
    <v-jumbotron 
          src="/static/images/bg.jpg"
          :gradient="gradient"
          dark >
      <v-container fill-height>
        <v-layout align-center>
          <v-flex>
            <h3 class="display-3">Welcome to the site</h3>
            <span class="subheading">Lorem ipsum dolor sit amet, pri veniam forensibus id. Vis maluisset molestiae id, ad semper lobortis cum. At impetus detraxit incorrupte usu, repudiare assueverit ex eum, ne nam essent vocent admodum.</span>
            <v-divider class="my-3"></v-divider>
            <div class="title mb-3">Check out our newest features!</div>
            <v-btn large color="primary" class="mx-0">See more</v-btn>
          </v-flex>
        </v-layout>
      </v-container>
    </v-jumbotron> 
    <v-container fluid>
      <a href="http://localhost:3000/test">lorem</a>
    </v-container>
  </div>
</template>

<script>
export default {
    data: () => ({
      gradient: 'to top right, rgba(63,81,181, .7), rgba(25,32,72, .7)'
    })

}
</script>

<style>

</style>
