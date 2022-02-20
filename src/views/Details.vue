<template>
  <container>
   
    <div v-for="(prd, index) in detail_product" :key="index">
      <div v-if="prd.id === proId" class="">
        <v-img
          contain
          max-height="245"
          max-width="400"
          :src="prd.img_pic"
          class="position_size float-sm-left"
        ></v-img>

        <h1  class="position_text">
          {{ prd.pro_name }}
        </h1>
        <h1  class="position_text mb-5">{{ prd.price }}บาท</h1>

        <p class="position_text mb-5">
          รายละเอียดสินค้า : {{ prd.tell }}
        </p>
        
      </div>
    </div>
  </container>
</template>

<script>

export default {
  name: "detail",
  
  data() {
    return {
      show: false,
      proId: this.$route.params.Pid,
      idP: "hello",
      detail_product: [
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
      
    };
  },
  methods:{
    
  }
};
</script>

<style>
.position_size {
  margin: 30px;
  
}
.position_text{
  position: relative; 
  left: 30px; 
  font-size: 30px;
}
</style>