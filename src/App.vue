<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline">
        <span v-text="greeting"></span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>

    <v-content>
      <Dashboard/>
    </v-content>
  </v-app>
</template>

<script>
import Dashboard from "./components/Dashboard";

export default {
  name: "App",
  components: {
    Dashboard
  },
  computed: {
    greeting: function() {
      var dayPart = "";
      var hourOfDay = new Date().getHours();
      if (hourOfDay >= 4 && hourOfDay < 12) {
        dayPart = "morning";
      } 
      else if(hourOfDay >= 12 && hourOfDay < 17) {
        dayPart = "afternoon";
      }
      else if(hourOfDay >= 17 && hourOfDay < 22){
        dayPart = "evening";
      }
      else if (hourOfDay >= 22) {
        dayPart = "night";
      }
      else {
        return "You should go to bed Meredith.";
      }


      return "Good " + dayPart + ", Meredith!"


    }
  },
  data() {
    return {
      //
    };
  }
};
</script>
