<template>
  <div>
    
    <v-row no-gutters>
      <v-col v-for="(product, index) in list_product" :key="index" cols="sm">
        <v-card class="pa-2 mx-auto mb-5" outlined tile max-width="400">
          <v-img
            class="white--text align-end"
            height="200px"
            :src="product.img_pic"
          >
          </v-img>
          <v-card-title class="name_font">
            <h3>{{ product.pro_name }}</h3>
          </v-card-title>

          <v-card-text class="text--primary">
            <h2>{{ product.price }}บาท</h2>

            <div>{{ product.tell }}</div>
          </v-card-text>

          <v-card-actions>
            <v-spacer />
            <v-btn color="primary" text class="justify-center" @click="explor(product.id)">See</v-btn>
            <v-spacer />
            <v-btn color="success" elevation="3" rounded x-large class="" @click="buy_TOaddMoney(product.price)">Buy</v-btn>
         </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Allproduct",
  data: () => ({
    list_product: [
      {
        id: "001",
        pro_name: "coke",
        price: 13,
        img_pic:
          "https://namyapoocm.com/wp-content/uploads/2021/10/80.jpg.webp",
        tell: "coke",
      },
      {
        id: "002",
        pro_name: "c-vitt",
        price: 16,
        img_pic: "https://namyapoocm.com/wp-content/uploads/2021/10/90.jpg.webp",
        tell: "C-VITT ",
      },
      {
        id: "003",
        pro_name: "coconut",
        price: 23,
        img_pic: "https://namyapoocm.com/wp-content/uploads/2021/10/79.jpg.webp",
        tell: "โคโค่แม็กน้ำมะพร้าว",
      },
      {
        id: "004",
        pro_name: "เป๊ปซี่",
        price: 20,
        img_pic:
          "https://namyapoocm.com/wp-content/uploads/2021/10/101.jpg.webp",
        tell: "เป๊ปซี่",
      }
    ],
  }),
  methods:{
    explor(i){
       this.$emit("explor_pro",i);
    
    },
    buy_TOaddMoney(i){
      
      this.$emit("buy",i);
    }
  }
};
</script>

<style>
.name_font {
  color: black;
}
.position {
  position: relative;
  left: 280px;
}
</style>