<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="6">
        <v-card>
          <v-card-text>
            <v-table>
              <thead>
                <tr>
                  <th class="text-center">Марка</th>
                  <th class="text-center">Цена</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="item in concrete" :key="item.name">
                  <td class="text-center">{{ item.name }}</td>
                  <td class="text-center">{{ item.price }}</td>
                </tr>
              </tbody>
            </v-table>
          </v-card-text>
          <v-divider></v-divider>
          <v-card-actions>
            <v-btn color="amber darken-2" block variant="tonal">Заказать</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="12" md="6" class="d-none d-md-block">
        <h2 class="mb-3">Почему выбирают нас?</h2>
        <v-divider class="mb-3"></v-divider>

        <ul>
          <h3 class="mb-5">
            Оперативная подача: Гарантируем быструю доставку товарного бетона на
            ваш объект.
          </h3>
          <h3 class="mb-5">
            Собственный парк автобетононасосов: Наши машины обеспечивают
            бесперебойную и точную подачу бетона.
          </h3>
          <h3 class="mb-5">
            Высокое качество бетона: Мы используем только проверенные материалы
            для изготовления товарного бетона.
          </h3>
          <h3 class="mb-5">
            Надежность и профессионализм: Многолетний опыт и квалифицированные
            специалисты гарантируют успешное выполнение вашего заказа.
          </h3>
        </ul>
      </v-col>
    </v-row>
  </v-container>
</template>
  
  <script>
export default {
  name: "TableCard",

  data() {
    return {
      concrete: [
        {
          name: "B 5 (М-50)",
          price: "3 100 ₽",
        },
        {
          name: "B 7,5 (М-100)",
          price: "3 100 ₽",
        },
        {
          name: "B 10 (М-150)",
          price: "3 100 ₽",
        },
        {
          name: "B 15 (М-200)",
          price: "3 100 ₽",
        },
        {
          name: "B 22,5 (М-300)",
          price: "3 100 ₽",
        },
        {
          name: "B 25 (М-350)",
          price: "3 100 ₽",
        },
        {
          name: "B 30 (М-400)",
          price: "3 100 ₽",
        },
      ],
    };
  },
};
</script>
