<template>
  <div>
      <h3>Total: {{buy}}บาท </h3>
  </div>
</template>

<script>
export default {
    props: ["buy"],
  data() {
    return {
        total:0,
        
    };
  },
  methods:{
      
 
  },
  computed:{

  }
};
</script>

<style>
</style>