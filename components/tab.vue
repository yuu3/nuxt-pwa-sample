<template>
  <!-- Tab -->
  <v-card height="56px" flat dark >
    <v-bottom-nav :value="true" absolute color="transparent"> 
      <v-btn v-for="item in tabItem" :key="item.id" router :to="item.to" color="#1976d2" flat >
        <span>{{ item.text }}</span>
        <v-icon>{{ item.icon }}</v-icon>
      </v-btn>
    </v-bottom-nav>
  </v-card>
</template>

<script>
export default {
  name: 'tab',
  data() {
    return {
      tabItem: [
        {
          text: 'Home',
          icon: 'home',
          to: '/'
        },
        {
          text: 'Phote',
          icon: 'today',
          to: '/page1'
        },
        {
          text: 'Favorite',
          icon: 'favorite',
          to: '/page2'
        },
      ],
    }
  }
}
</script>