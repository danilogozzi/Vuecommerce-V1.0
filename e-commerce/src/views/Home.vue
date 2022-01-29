<template>
  <div id="home">
    <Homeslider />
    <div id="showcase">
      <ul v-for="(p, id) in products" :key="id">
        <li id="product-box">
          <a @click="selectProduct(id, $event)" :href="anchorDetailProd">
            <img id="img-product" :src="p.imgProduct" alt="" />
          </a>
          <br />
          <a>
            <span
              ><h4 class="m-1">{{ p.name }}</h4></span
            >
          </a>
          <br />
          <a>
            <span
              ><p>{{ p.description }}</p></span
            >
          </a>
          <br />
          <a>
            <span>R${{ p.value }}</span>
          </a>
          <hr />
          <div class="container d-flex justify-content-center">
            <div class="row">
              <div class="col-md-10 d-flex justify-content-end">
                <button>Add to Cart</button>
              </div>
              <div class="col-md-2 d-flex justify-content-end">
                <select name="" id="product-qtd">
                  <option value="1">1</option>
                  <option value="2">2</option>
                  <option value="3">3</option>
                  <option value="4">4</option>
                  <option value="5">5</option>
                  <option value="6">6</option>
                  <option value="7">7</option>
                  <option value="8">8</option>
                  <option value="9">9</option>
                </select>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Homeslider from "../components/Homeslider.vue";

export default {
  name: "Home",
  components: { Homeslider },
  props: {
    products: {
      type: Array,
      required: true,
    },
    selectedProduct:{
      type:Number,
      required:true
    }
  },
  data() {
    return {
      anchorDetailProd:'',
      selectedProductActual:this.selectedProduct
    };
  },
  methods:{
    selectProduct(id){
        console.log(`Posição ${id}`+` Produto Selecionado ${this.selectedProductActual = id}`,this.anchorDetailProd = `/product_detail/${this.selectedProductActual}`)
    }
  }
};
</script>
<style>
#product-box:hover {
  border: 1px solid rgb(110, 196, 218);
}
#product-box a {
  color: black;
  text-decoration: none;
}
#product-box {
  list-style: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 30rem;
  height: 41rem;
  margin: 0.5rem;
  border-bottom: 1px solid #0001;
  border-right: 1px solid #0001;
  box-shadow: 1px 1px 1px #0002;
  cursor: pointer;
  text-align: center;
  border-radius: 10px;
}
#showcase {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
}
#img-product {
  width: 100%;
}
#product-box select {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  cursor: pointer;
}
#product-box button:hover {
  background-color: #29bda4da;
}
#product-box button {
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  border: 1px solid #0005;
  background-color: #00c4a7;
  color: white;
  height: 2.5rem;
  width: 6rem;
  cursor: pointer;
  box-shadow: 0;
  outline: none;
}
</style>