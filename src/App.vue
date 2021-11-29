<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <Atitulo
        :alt="'Componentes Vue CDN A CLI'"
        :src="'https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png'"
        :style="{ width: '40px', height: '40px' }"
      />
      <v-container>
        <h3>Componentes Vue CDN A CLI</h3>
      </v-container>
    </v-app-bar>

    <v-main>
      <div class="mt-5 pt-1">
        <v-container class="spacing-playground pa-6" fluid>
          <v-row>
            <TableList
              :lists="fruits"
              :titulo="'Lista de Frutas'"
              :mostrar="6"
              :dimg="dimg"
              :heads="['#', 'Fruta', 'Precio', 'Imagen', 'Descripción']"
              :styles="{
                head: 'orange lighten-4',
                
                row: {
                  color1: 'red lighten-4',
                  color2: 'light-green lighten-4',
                },
              }"
            />

            <TableList
              :lists="cereals"
              :titulo="'Lista de Cereales'"
              :mostrar="6"
              :dimg="dimg"
              :heads="['#', 'Cereales', 'Precio', 'Imagen', 'Descripción']"
              :styles="{
                head: 'grey lighten-2',
               
                row: { color1: 'cyan lighten-4', color2: 'white' },
              }"
            />
            <TableList
              :lists="literarys"
              :titulo="'Lista de Libros'"
              :mostrar="6"
              :dimg="dimg"
              :heads="['#', 'Libros', 'Precio', 'Imagen', 'Descripción']"
              :styles="{
                head: 'amber darken-2',
            
                row: { color1: 'amber lighten-4', color2: 'grey lighten-5' },
              }"
            />
          </v-row>
        </v-container>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import Atitulo from "./components/Atitulo";
import TableList from "./components/TableList";

export default {
  name: "App",
  components: {
    Atitulo,
    TableList,
  },

  data: () => ({
    dimg: {
      h: 150,
      w: 150,
    },
    fruits: [
      {
        id: 1,
        name: "Papaya",
        price: 1.0,
        image:
          "https://images.pexels.com/photos/701969/pexels-photo-701969.jpeg",
        description: "",
      },
      {
        id: 2,
        name: "Uva",
        price: 1.2,
        image:
          "https://images.pexels.com/photos/5529558/pexels-photo-5529558.jpeg",
        description: "",
      },
      {
        id: 3,
        name: "Melón",
        price: 2.1,
        image:
          "https://images.pexels.com/photos/1100419/pexels-photo-1100419.jpeg",
        description: "",
      },
    ],
    cereals: [
      {
        id: 1,
        name: "Arroz",
        price: 10,
        image:
          "https://images.pexels.com/photos/7421207/pexels-photo-7421207.jpeg",
        description: "Es de consumo diario",
      },
      {
        id: 2,
        name: "Trigo",
        price: 22.5,
        image:
          "https://images.pexels.com/photos/6412600/pexels-photo-6412600.jpeg",
        description: "Es un super alimento",
      },
      {
        id: 3,
        name: "Maiz",
        price: 50.1,
        image:
          "https://images.pexels.com/photos/547264/pexels-photo-547264.jpeg",
        description: "",
      },
    ],
    literarys: [
      {
        id: 1,
        name: "Historia UNiversal",
        price: 100,
        image:
          "https://images.pexels.com/photos/1005324/literature-book-open-pages-1005324.jpeg",
        description: "",
      },
      {
        id: 2,
        name: "Literatura Universal",
        price: 220.5,
        image: "https://images.pexels.com/photos/34627/pexels-photo.jpg",
        description: "",
      },
      {
        id: 3,
        name: "Desarrollo Humano",
        price: 250.1,
        image:
          "https://images.pexels.com/photos/1106468/pexels-photo-1106468.jpeg",
        description: "",
      },
    ],
  }),
};
/* data() {
    return {
      dimg: {
        h: 150,
        w: 150,
      },
      fruits: [
        {
          id: 1,
          name: "Papaya",
          price: 1.0,
          image:
            "https://images.pexels.com/photos/701969/pexels-photo-701969.jpeg",
          description: "",
        },
        {
          id: 2,
          name: "Uva",
          price: 1.2,
          image:
            "https://images.pexels.com/photos/5529558/pexels-photo-5529558.jpeg",
          description: "",
        },
        {
          id: 3,
          name: "Melón",
          price: 2.1,
          image:
            "https://images.pexels.com/photos/1100419/pexels-photo-1100419.jpeg",
          description: "",
        },
      ],
    };*/
</script>
