<template>
  <v-app light>
    <!--DRAWER-->
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      flat
      class="color-purple"
    >
    
    </v-navigation-drawer>
  <!--APP BAR UP-->
    <v-app-bar
      :clipped-left="clipped"
      app
      flat
      class="color-green-second"
    >
      <v-app-bar-nav-icon class="d-lg-none d-xl-flex" @click.stop="drawer = !drawer" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
        class="d-none d-md-flex"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-toolbar-title class="font-abel" v-text="title" />
       
      <v-spacer />
     <profile/>
    </v-app-bar>
<!--CONTENT PAGE-->
    <v-content style="background-color:white">
      <nuxt/>
    </v-content>



  </v-app>
</template>

<script>
import profile from "@/components/appbar/profile";
export default {
  data () {
    return {
      clipped: false,
      drawer: true,
      miniVariant: true,
      right: true,
      rightDrawer: false,
      title: 'ReadMe.txt'
    }
  },
  components:{
    profile
  }
}
</script>

<style>

.h-default{
  height :50px;
}

</style>