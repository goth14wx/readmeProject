<template>
  <v-app  class="default-background">
    <!--DRAWER-->
    <v-navigation-drawer
    expand-on-hover
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      flat
      class="color-instagram-gradient"
    >
      <list/>
    </v-navigation-drawer>
  <!--APP BAR UP-->
    <v-app-bar
      :clipped-left="clipped"
      app
      flat
      class="color-green-second"
      height="70px"
    >
      <v-app-bar-nav-icon class="d-lg-none d-xl-flex" @click.stop="drawer = !drawer" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
        class="d-none d-md-flex"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-toolbar-title class="font-sf-regular" v-text="title" />
       
      <v-spacer />
    <toolbar/>
     <profile/>
    </v-app-bar>
<!--CONTENT PAGE-->
    <v-content style="background-color:white">
     <breadcrums class="color-green-second" />
      <nuxt/>
    </v-content>



  </v-app>
</template>

<script>
import profile from "@/components/appbar/profile";
import toolbar from "@/components/appbar/toolbar";
import list from "@/components/drawer/list";
import breadcrums from "@/components/dashboard/breadcrums";
export default {
  data () {
    return {
      clipped: false,
      drawer: true,
      miniVariant: true,
      right: true,
      rightDrawer: false,
      title: 'readMe'
    }
  },
  components:{
    profile,
    toolbar,
    list,
    breadcrums
  }
}
</script>

<style>

.h-default{
  height :50px;
}

</style>