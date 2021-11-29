<template>
  <v-col cols="12" :lg="mostrar" :md="mostrar">
    <v-card>
      <v-card-title>{{ titulo }}</v-card-title>
      <v-card-text>
        <v-simple-table >
          <template v-slot:default>
            <thead>
              <tr :class="styles.head">
                <th scope="col" v-for="(head, i) in heads" :key="i">
                  {{ head }}
                </th>
              </tr>
            </thead>
            <tbody>
              <tr
                v-for="(list, i) in lists"
                :key="i"
                :class="i % 2 == 0 ? styles.row.color1 : styles.row.color2"
              >
                <td>{{ list.id }}</td>
                <td>{{ list.name }}</td>
                <td class="price">{{ list.price}}</td>
                <td>
                  <v-img
                    :src="list.image + '?h=' + dimg.h + '&w=' + dimg.w"
                    class="img-fluid img-thumbnail"
                    alt=""
                  />
                </td>
                <td>{{ list.description }}</td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
      </v-card-text>
    </v-card>
  </v-col>
</template>

<script>
export default {
 
  props: {
    heads: { type: Array },
    lists: { type: Array },
    styles: { type: Object },
    dimg: { type: Object },
    titulo: { type: String, default: "" },
    mostrar: { type: Number, default: 6 },
  },
 
};
</script>

<style lang="scss" scoped>

.price {
  text-align: end;
}

</style>
