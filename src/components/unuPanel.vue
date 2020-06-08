<template>
  <v-expansion-panels class="green"
                      multiple
                      v-model="nPaneluri"
  >
    <!-- <v-expansion-panel class="mb-2 " -->
    <v-expansion-panel class="mb-1"
       v-for="(ao,k) in obArr"
       :key='k'
    >
      <!-- <v-expansion-panel-header class='my-n2' -->
      <v-expansion-panel-header class='my-n2'
      
       ><strong > {{k}} - lung: {{ao.length}} </strong> </v-expansion-panel-header>
         <v-sheet class='blue lighten-3 mx-0 card-body' 
                >
              <v-expansion-panel-content  
                  class='yellow padmic'
                  v-for="(obj,i) in ao"
                  :key='i'
              >
            
     <!-- -------------------------------------------------------------- -->
          <!-- <v-item-group> -->
                  <v-checkbox v-model="bifatele" 
                              :label="`${i+1}: ${obj.numele}`"
                              value="xxx"
                             hide-details 
                             class="title"
                             dense
                  ></v-checkbox>
       
              </v-expansion-panel-content>
        
      </v-sheet>
    </v-expansion-panel>
  </v-expansion-panels>
</template>
<script>

export default {
  data () {
   return {
     nPaneluri:[0,1,2,3,4],
     obArr:{},
     bifatele:[]
     }
  },
  created(){
    this.obArr=instanta.objRezultat ;
  }
}
</script>
<style>
.card-body {
  overflow-y: auto;
  max-height: 35vh;
}  
 .padmic {
      padding-bottom: 2px;
    }
</style>
