<template>

<v-container fluid>
    <v-row>
        <v-col cols="6" class="text-truncate text-center" v-for="(item,n) in items" :key="'itemDashboardItem'+n">
           <v-hover v-slot:default="{hover}">
               <v-btn class="ma-2" large="" :elevation="hover ? 7: 2" tile outlined color="white">
      <v-icon left>{{item.icon}}</v-icon> {{item.title}}
    </v-btn>
           </v-hover>
        </v-col>
    </v-row>
</v-container>

</template>

<script>
  export default {
    data: () => ({
      items: [
        {
            title:"clases",
            icon:"class"
        },
         {
            title:"Cursos",
            icon:"subject"
        }
      ],
    }),
  }
</script>