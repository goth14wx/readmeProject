<template>
   <v-card flat color="transparent">
        <v-list
        flat
        tile=""
      >
        <v-list-item link v-for="(item,n) in itemList" :key="'listDrawerItem'+n">
          <v-list-item-icon>
            <v-icon>{{item.icon}}</v-icon>
          </v-list-item-icon>
          <v-list-item-title>{{item.title}}</v-list-item-title>
          
          <v-divider></v-divider>
        </v-list-item>
      </v-list>
   </v-card>
</template>

<script>
export default {
  data:()=>({
    itemList:[
      {
        title:"Cursos",
        icon:"subject"
      },
      {
        title:"Clases",
        icon:"class"
      }
    ]
  })
}
</script>