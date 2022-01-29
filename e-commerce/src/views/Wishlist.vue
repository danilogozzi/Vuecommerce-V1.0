<template>
  <div class="wishlist">
    <h3>Your Wishlist</h3>
    <ul v-for="(p, i) in products" :key="i">
      <li id="product-box-wishlist">
        <img id="img-product-wishlist" :src="p.imgProduct" alt="" />
        <br />
        <span
          ><h4 class="m-1">{{ p.name }}</h4></span
        >
        <br />
        <span
          ><p>{{ p.description }}</p></span
        >
        <br />
        <span>R${{ p.value }}</span>
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
</template>

<script>
export default {
  props: {
    products: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>

<style>
.wishlist h3 {
  align-self: center;
}
.wishlist::-webkit-scrollbar-thumb:hover{
  background: #888;
}
.wishlist::-webkit-scrollbar-thumb{
  background: rgb(110, 196, 218);
}
.wishlist {
  display: flex;
  padding: 2rem;
  flex-shrink: row wrap;
  width: 100%;
  overflow-x: scroll;
}
#img-product-wishlist {
  width:22rem;
}
#product-box-wishlist select {
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  cursor: pointer;
}
#product-box-wishlist:hover {
  border: 1px solid rgb(110, 196, 218);
}
#product-box-wishlist a {
  color: black;
  text-decoration: none;
}
#product-box-wishlist {
  list-style: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 24rem;
  height: 37rem;
  margin: 0.5rem;
  border-bottom: 1px solid #0001;
  border-right: 1px solid #0001;
  box-shadow: 1px 1px 1px #0002;
  cursor: pointer;
  text-align: center;
  border-radius: 10px;
}
#product-box-wishlist button:hover {
  background-color: #29bda4da;
}
#product-box-wishlist button {
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