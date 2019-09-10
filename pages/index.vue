<template>
<v-container fluid class="color-green-gradient-medium pt-0">
    <!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop -->
    <v-row class="color-green-second pt-0">
      <v-col
      cols="12"
      >
      </v-col>
    </v-row>
    <v-row class="color-green-second pt-0">
      <v-col
        v-for="n in 3"
        :key="n"
        cols="12"
        md="4"
        sm="4"
      >
        <v-card
          class="pa-3 ma-1"
          tile
          color="white black--text"
        >
          .col-6 .col-md-4
        </v-card>
      </v-col>
    </v-row>

    <!-- Columns are always 50% wide, on mobile and desktop -->
    <v-row class="color-green-gradient-medium pt-0">
      <v-col
        v-for="n in 2"
        :key="n"
        cols="6"
        
      >
        <v-card
          class="pa-2"
          outlined
          tile
        >
          .col-6
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import cardTest from "@/components/card-test";
export default {
  data:(()=>{

  }),
  components:{
      cardTest
  }
}
</script>