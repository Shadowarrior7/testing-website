<template>
  <v-app>
    <!-- Link to Material Icons-->
    <link
      href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Material+Icons"
      rel="stylesheet"
      type="text/css"
    />
    
    <!-- TODO: Add an AppBar component here -->
    <!-- Make sure to pass in the user object as a prop. -->
    

    <v-main>
      <router-view :user="user"></router-view>
    </v-main>

  </v-app>
</template>

<script>
// TODO: Import the app bar component here
// HINT: When writing your import path, you can use the `@` symbol
// to jump straight to the `src` folder instead of trying to figure
// out how to do a relative path. Also, if you're trying to access
// a JavaScript file called `index.js`, you can skip the entire file
// name and just use the containing folder's name; e.g.:
// import thing from '@/util'
// is the same as:
// import thing from '../src/util/index.js'
// Remember, this only works for files called `index.js`. `.vue` files
// must be imported with the entire file name, including the extension.
// e.g.:
// import MyComponent from '@/components/MyComponent.vue'
// You can delete or move these comments if you'd like.


export default {
  name: 'App',
  components: {
    // TODO: Use the Vue Documentation to find out how to use this property
    
  },
  data:()=> ({
    user: {
    },
    defaultUser: {
      UserName: 'hello'
    }}
    ),
    methods: {
     async getUser(){ //this function updates the user variable with a fetch request
       // TODO: Use fetch() to get the user from your API
        // Make sure to include your credentials in the request
        // Also you might want to still return an object identical
        // to the `default` below if the fetch() fails
    }
    },
    mounted(){ // this is used to call getUser when the page loads 
      this.getUser()
    }     
}
</script>