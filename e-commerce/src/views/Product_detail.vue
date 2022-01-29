<template>
  <div>
    <ul v-for="(p, id) in products" :key="id" id="product-detail">
      <li id="product-box-detail">
        <img
          @click="confirmActual()"
          id="img-product-detail"
          :src="p.imgProduct"
          alt=""
        />
        <div id="cx-product-detail">
          <span
            ><h4 class="m-1">{{ p.name }}</h4></span
          >
          <span
            ><p>{{ p.description }}</p></span
          >
          <span>R${{ p.value }}</span>

          <div class="container d-flex justify-content-end">
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
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    products: {
      type: Array,
      required: true,
    },
    selectedProduct: {
      type: Number,
      required: true,
    },
  },
  data() {
    return {
      selectedProductActual: this.selectedProduct,
    };
  },
  methods: {
    confirmActual() {
      console.log(this.selectActualProduct);
    },
  },

};
</script>

<style>
#product-box-detail {
  list-style: none;
  display: flex;
  flex-direction: row;
  border-bottom: 1px solid #0002;
  border-right: 1px solid #0001;
  padding: 0 0 2rem 0;
  box-shadow: 1px 4px 1px 2px #0001;
}
#product-detail {
  padding: 2rem;
}
#img-product-detail {
  width: 30rem;
  height: 30rem;
}
#cx-product-detail {
  display: flex;
  flex-direction: column;
  width: 70%;
  margin: 0 auto;
}
#product-box-detail select {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  cursor: pointer;
}
#product-box-detail button:hover {
  background-color: #29bda4da;
}
#product-box-detail button {
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