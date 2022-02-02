<template>
  <v-app>
    <v-app-bar flat
      app
      color="white"
      height="100"
    >
    <v-layout align-center>
        <v-flex>
             <v-text-field 
                placeholder="Search"
                color="grey"
                solo-inverted 
                filled  
                class="mt-7" 
                flat 
                solo
                prepend-inner-icon="mdi-magnify"
                />
        </v-flex >
            <v-btn height="45" class="mx-2 ml-4">
                <v-icon>mdi-compare-vertical</v-icon>
            </v-btn>
            <v-btn height="45" class="ml-2" dark>
                <v-icon>mdi-plus</v-icon>
            </v-btn>
      
       
    </v-layout>
      

    </v-app-bar>

    <v-navigation-drawer app permanent>
      <v-list-item>
          <v-list-item-avatar>
              <v-img 
                    width="10"
                    lazy="https://i.pinimg.com/originals/86/0c/87/860c87633f4de3aae800d9c948cbebdd.png" 
                    src="https://i.pinimg.com/originals/86/0c/87/860c87633f4de3aae800d9c948cbebdd.png" 
                     />
          </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="title">
              <v-layout align-center> Pinterest
              </v-layout>
          </v-list-item-title>
          
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <div class="mx-2 subtitle-2 grey--text">Insghts</div>
      <v-list
        dense
        nav
      >
        <v-list-item
          link
        >
          <v-list-item-icon>
            <v-icon>mdi-mail</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Messages</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
     
      <v-list-item
          link
        >
          <v-list-item-icon>
            <v-icon>mdi-bell</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Notification</v-list-item-title>
          </v-list-item-content>
          <v-list-item-avatar 
          size="25" color="orange" 
          class="white--text subtitle-2 ml-2 align-center">
          <v-flex text-center>2</v-flex>
          </v-list-item-avatar>
        </v-list-item>   
        </v-list> 
        <v-card flat>
            <v-img
             src="https://assets.website-files.com/5bff8886c3964a992e90d465/5bff98f85ea7faf86504605e_scenes.gif" />
            <v-layout class="pt-2 px-8">
                <v-flex text-center>
                    <div class="subtitle-2 blue--text">Unclock Business Tools</div>
                    <div class="caption">Hurry Up! Now you can unclokc out new business tools at your  Convience</div>
                </v-flex>
            </v-layout>
        </v-card>   
            <v-layout  align-center class="my-8 mx-4">
                <v-card 
                style="border-radius: 8px" 
                class="mx-auto px-3 py-3"
                 elevation="5">
                    <v-list-item>
                        <v-list-item-avatar>
                            <v-img src="https://images.unsplash.com/flagged/photo-1578074611062-4387baa90b42?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzY4fHxwcm9maWxlJTIwaW1nJTIwdXJsfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=400&q=60">
                            </v-img>
                        </v-list-item-avatar>
                        <v-list-item-content>
                            <v-list-item-title class="subtitle-2">Islom Rakhimkulov</v-list-item-title>
                            <v-list-item-title>Frontend Software Engineer </v-list-item-title>
                        </v-list-item-content>
                        <v-list-action>
                            <v-icon>mdi-chevron-right</v-icon>
                        </v-list-action>
                    </v-list-item>
                </v-card>
            </v-layout>

    </v-navigation-drawer>

    <v-main>
      <HomePage/>
    </v-main>
  </v-app>
</template>

<script>
import HomePage from "@/pages/HomePage.vue";
export default {
    name: "MainLayout",
    components: {
        HomePage
    },
    data: () => ({
        items: [
          { title: 'Home', icon: 'mdi-home' },
          { title: 'Recnent', icon: 'mdi-clock-time-three' },
          { title: 'Following', icon: 'mdi-account-group' },
        ],
        items2: [
          { title: 'Messages', icon: 'mdi-view-dashboard' },
          { title: 'Notification', icon: 'mdi-image' },
        ],
        right: null,
    })
}
</script>

<style>

</style>