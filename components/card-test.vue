<template>
  <v-card light="" 
            class="ma-1 "
            color="transparent"
            outlined
            tile>
             <v-card-title  class="font-sf-regular"><slot name="title"></slot></v-card-title>
             <v-divider class="mx-4" />
    <v-card-text>
      <list/>
    </v-card-text>
    <v-card-actions>
      <v-btn text>Click</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
import list from "@/components/dashboard/list";
export default{
  data(){
    return{
    }
  },
  components:{
    list
  }
}
</script>