<template>
    <v-app >
        <v-container fluid>
            <!-- breadcrumbs -->
            <v-breadcrumbs :items="breadcrumbItems" class="dark--text">
            <template v-slot:divider>
                <v-icon>mdi-chevron-right</v-icon>
            </template>
            </v-breadcrumbs>
            <!-- breadcrumbs End-->

            <!-- Cards -->
            <v-row dense>
                <v-col>
                <v-card>
                    <div class="d-flex flex-no-wrap justify-space-between my-5px">
                      <div>
                        <v-card-title class="headline">User Profile</v-card-title>
                        <v-card-subtitle ></v-card-subtitle>
                        <v-card-text>
                          <h3 class=" text--primary mb-5" v-if="user">Name : Jhon Doe</h3> 
                          <h3 class="text--primary" v-if="user">Email : jhon@gmail.com</h3>  
                        </v-card-text>
                        <v-card-actions>
                        </v-card-actions>
                      </div>
                    </div>
                </v-card>
                </v-col>
            </v-row>
            <!-- Cards Ends-->
            <br>
        </v-container>
    </v-app>
</template>

<script>
  export default {
    data () {
      return {
        user: null,
        breadcrumbItems: [
        {
          text: 'Profile',
          disabled: true,
        },
      ],
    }
  },
  mounted(){
    document.title = 'Techminate | Profile'
    
  },

  methods:{
      
  }
  }
</script>