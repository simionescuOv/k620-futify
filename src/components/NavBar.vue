<template>
<nav>
  <v-navigation-drawer app
                       v-model="sertar"  >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>

        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <!-- <v-icon>{{item.icon}}</v-icon> -->
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
  </v-navigation-drawer>
  <v-app-bar app>
     <v-app-bar-nav-icon @click.stop="sertar = !sertar"
      
     ></v-app-bar-nav-icon>
     <v-icon>mdi-heart</v-icon>

  </v-app-bar>
</nav>
</template>

<script>
  export default {
    data () {
      return {
          sertar: false,
        items: [
          { title: 'Home', icon: 'mdi-account' },
          { title: 'About', icon: 'mdi-information-variant' },
        ],
      }
    },
  }
</script>
