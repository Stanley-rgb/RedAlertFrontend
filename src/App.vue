<template>
  <v-app>

    <v-main>
      <SignUpPage/>
    </v-main>
    <v-content>
      <router-view></router-view>
    </v-content>
    
  </v-app>
</template>

<script>

import SignUpPage from './components/SignUpPage';
export default {
  name: 'App',

  components: {
    SignUpPage,
  },

  data: () => ({
    //
  }),
};
</script>
