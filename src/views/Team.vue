<template>
  <div class="team">
    <h1 class="subtitle-2 grey--text">Team</h1>

    <v-container class="my-10">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card flat class="text-center grey lighten-2 ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="pink">
                <img :src="person.avatar">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subtitle-1 red--text darken-4">{{ person.name }}</div>
              <div class="orange--text darken-3">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn plain color="purple accent-4">
                <v-icon left>message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    team: [
      {
        name: 'The Net Ninja',
        role: 'Web developer',
        avatar: 'https://raw.githubusercontent.com/iamshaunjp/vuetify-playlist/lesson-20/todo-ninja/public/avatar-1.png'
      },
      {
        name: 'Ryu',
        role: 'Graphic designer',
        avatar: 'https://raw.githubusercontent.com/iamshaunjp/vuetify-playlist/lesson-20/todo-ninja/public/avatar-2.png'
      },
      {
        name: 'Chun Li',
        role: 'Web developer',
        avatar:
            'https://raw.githubusercontent.com/iamshaunjp/vuetify-playlist/lesson-20/todo-ninja/public/avatar-3.png'
      },
      {
        name: 'Gouken',
        role: 'Social media maverick',
        avatar:
            'https://raw.githubusercontent.com/iamshaunjp/vuetify-playlist/lesson-20/todo-ninja/public/avatar-4.png'
      },
      {
        name: 'Yoshi',
        role: 'Sales guru',
        avatar:
            'https://raw.githubusercontent.com/iamshaunjp/vuetify-playlist/lesson-20/todo-ninja/public/avatar-5.png'
      }
    ]
  })
}
</script>

<style scoped>

</style>