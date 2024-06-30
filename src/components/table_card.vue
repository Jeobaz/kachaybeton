<template>
    <v-col cols="xs-1"><v-card>
        <v-card-title class="headline">Товарный бетон</v-card-title>
      <v-divider></v-divider>
      <v-card-text>
        <v-table>
    <thead>
      <tr>
        <th class="text-center">
          Марка
        </th>
        <th class="text-center">
          Цена
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in concrete"
        :key="item.name"
      >
        <td class="text-center">{{ item.name }}</td>
        <td class="text-center">{{ item.price }}</td>
      </tr>
    </tbody>
  </v-table>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <v-btn color="amber darke2-3" block varitant="tonal">Заказать</v-btn>
      </v-card-actions>
    </v-card></v-col>
    
  </template>
  
  <script>
  export default {
    name: 'TableCard',
   
    data() {
      return {
        concrete: [
          {
            name: 'B 5 (М-50)',
            price: "3 100 ₽",
          },
          {
            name: 'B 7,5 (М-100)',
             price: "3 100 ₽",
          },
          {
            name: 'B 10 (М-150)',
             price: "3 100 ₽",
          },
          {
            name: 'B 15 (М-200)',
             price: "3 100 ₽",
          },
          {
            name: 'B 22,5 (М-300)',
             price: "3 100 ₽",
          },
          {
            name: 'B 25 (М-350)',
             price: "3 100 ₽",
          },
          {
            name: 'B 30 (М-400)',
             price: "3 100 ₽",
          },
         
        ],
      };
    },
  };
  </script>
