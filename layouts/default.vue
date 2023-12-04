<template>
  <v-app>
  <v-card>
    <v-layout>
      <v-app-bar color="#c8b6c4" proeminent>
        <v-app-bar-nav-icon
          v-if="$vuetify.display.xs"
          variant="text"
          @click.stop="drawer = !drawer"
        ></v-app-bar-nav-icon>
        <v-toolbar-title>
        <div class="titleBar">
            <img src="..\assets\logot.png" alt="testeLog" height="50" />
            <p>
              DR. RAYANNE DOURADO
            </p>
        </div>
      </v-toolbar-title>
      </v-app-bar>

      <v-navigation-drawer :permanent="!$vuetify.display.xs" v-model="drawer" >
        <div class="menuList">
        <v-list active-color="#440824" active-class="active" :items="items" > 
        </v-list>
      </div>
      </v-navigation-drawer>
      <v-main style="height: 800px">
        <v-card-text>
          <div>
        
              <v-img
                src="..\assets\RayTerno (1).jpg"
                height="1000"
                
              ></v-img>

          </div>
          <h1>whathever</h1>
        </v-card-text>
      </v-main>
    </v-layout>
  </v-card>

  <v-footer
    class="text-center d-flex flex-column" color="#440824"
  >
    <div>
      <v-btn size="x-large"
        v-for="icon in icons"
        :key="icon"
        class="mx-4"
        :icon="icon"
        variant="text"
      ></v-btn>
    </div>

    <div class="pt-0">
      Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
    </div>

    <v-divider></v-divider>

    <div>
      {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
    </div>
  </v-footer>
  </v-app>

</template>
    
    <script>
export default {
  mounted() {
    if (!this.$vuetify.display.xs) {
      this.drawer = true;
    }
  },
  data() {
    return {
      drawer: false,
      items: [
        { title: "Sobre", value: "abobora"},
        { title: "Cuidados com x", value: "quiabo" },
        { title: "Consultas/Agendamentos", value: "vagem" },
        { title: "Portifolio", value: "arroz" },
      ],
       icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
        'mdi-instagram',
      ],
    };
  },
};
</script>

<style>
.titleBar {
  display: flex;
  align-items: center;
}
.menuList{
background-color: #440824; 
color: white; 
} 
.v-list-item:hover{
 background:white;
 color: #440824;
}
/* .v-list-item:active{
 background:#323285;
 color: aliceblue;
} */
.active{
  background: #c8b6c4;
  color: black;
}
</style>