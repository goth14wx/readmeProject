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
        v-for="(card,n) in cards"
        :key="n"
        cols="12"
        md="3"
        sm="6"
      >
       <v-hover v-slot:default="{ hover }">
        <v-card
        :elevation="hover ? 12 : 2"
          class="ma-3"
          color="white black--text"
          style="border-radius:10px"
        >
        <v-container >
    <!-- Stack the columns on mobile by making one full-width and the other half-width -->
    <v-row>
      <v-col
        cols="6"
        md="8"
        class="font-sf-light"
        style="text-align:center"
      >
     <h3 class="text-truncate" > {{card.title}}</h3>
     <h6 class="text-truncate text-muted">{{card.subtitle}}</h6>
      </v-col>
      <v-col 
       cols="6"
        md="4"
        style="text-align:center"
        >
         <v-icon large center :color="card.color">{{card.icon}}</v-icon>
      </v-col>
      </v-row>
      <v-row>
        <v-col>
          <h3>HOLA</h3>
        </v-col>
      </v-row>
        <v-btn
              absolute
              fab
              bottom
              right
              :color="card.color"
            >
              <v-icon>mdi-play</v-icon>
            </v-btn>
      </v-container>
        </v-card>
       </v-hover>
      </v-col>
    </v-row>

    <!-- Columns are always 50% wide, on mobile and desktop -->
    <v-row class="color-green-gradient-medium pt-0">
      <v-col
        v-for="(td,n) in todo"
        :key="n"
        cols="12"
        md="6"
      >
        <v-card
          class="pa-2"
          light
          outlined
          tile
          style="border-radius:10px"
        >
          <cardTest>
            <template v-slot:title>
              {{td.title}}
            </template>
          </cardTest>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import cardTest from "@/components/card-test";

export default {
  data(){
    return{
      cards:[
         {
            title:"Ahora, ¿Que sigue?",
            icon:"calendar_today",
            subtitle:"Que hay en tu agenda",
            color:"purple"
          },
          {
            title:"¿Donde Lo deje?",
            icon:"menu_book",
            subtitle:"Donde dejaste la lectura pasada",
            color:"green"
          },
          {
            title:"Ultimo quiz que tomaste",
            icon:"list_alt",
            subtitle:"Ultimo test que tomaste",
            color:"pink"
          },
          {
            title:"¿Segur@ lo terminaste?",
            icon:"create",
            subtitle:"Ultimos apuntes que tomaste",
            color:"yellow"
          }
      ],
      todo:[
        {
          title:"To-do List"
        },
        {
          title:"Ultimas Clases Agregadas"
        }
      ]
    }
  },
  components:{
      cardTest
  }
}
</script>

<style> 

</style>