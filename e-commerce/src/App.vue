<template>
  <div id="app">
    <div class="container-fluid">
      <header>
        <nav id="nav" class="row">
          <div id="store" class="col-md-5">
            <a href="/"><img :src="logo" id="logo" alt="logo" /></a>
            <input placeholder=" Search..." id="search" type="text" />
          </div>
          <div id="department" class="col-md-4">
            <router-link id="links" to="/">Home</router-link>
            <router-link id="links" to="/user/wishlist">Wishlist</router-link>
            <router-link id="links" to="/about">About</router-link>
          </div>
          <div id="user" class="col-md-3">
            <div id="social">
              <i class="fab fa-facebook"></i>
              <i class="fab fa-instagram"></i>
              <i class="fab fa-linkedin"></i>
              <i class="fab fa-twitter"></i>
            </div>
            <i class="fas fa-shopping-cart">0</i>
            <button><i class="fas fa-user-plus"></i> Sign Up</button>
            <button><i class="fas fa-user"></i> Log In</button>
          </div>
        </nav>
      </header>
    </div>
    <router-view :selectedProduct="selectedProduct" :products="products" />
    <footer id="footer">
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-6">
            <p>
              Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit
              amet.
            </p>
          </div>
          <div class="col-md-6 d-flex justify-content-center">
            <span>Made with ♥</span>
            <span>Vuecommerce |&nbsp;</span>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      selectedProduct: 0,
      logo: "https://ivanlori.github.io/Vuemmerce/_nuxt/img/vuemmerce-logo.6809a10.png",
      products: [
        {
          id: 1,
          name: "Product 1",
          value: 50,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 2,
          name: "Product 2",
          value: 100,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 3,
          name: "Product 3",
          value: 150,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 4,
          name: "Product 4",
          value: 200,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 5,
          name: "Product 5",
          value: 300,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 6,
          name: "Product 6",
          value: 350,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 7,
          name: "Product 7",
          value: 350,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 8,
          name: "Product 8",
          value: 350,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
        {
          id: 9,
          name: "Product 9",
          value: 350,
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit",
          favorite: false,
          imgProduct: "https://bulma.io/images/placeholders/1280x960.png",
        },
      ],
    };
  },
};
</script>
<style>
/* width */
::-webkit-scrollbar {
  width: 0.5rem;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 15px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: rgb(110, 196, 218);
}

body {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}
#store {
  display: flex;
  align-items: center;
}
#user button:hover {
  border: 1px solid rgb(0, 0, 0, 0.2);
}
#user button {
  border: 1px solid rgb(0, 0, 0, 0.1);
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  height: 2.5rem;
  cursor: pointer;
  background-color: white;
  padding: 0.5rem;
  box-shadow: 0 0 0 0;
  outline: 0;
}
#user i {
  cursor: pointer;
}
#user {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
}
#social i {
  margin: 0 5px;
  cursor: pointer;
  color: gray;
}
#search::placeholder {
  color: gray;
}
#search {
  margin: 0 2rem;
  height: 2.5rem;
  width: 100%;
  border: 1px solid rgb(0, 0, 0, 0.1);
  border-radius: 15px;
  box-shadow: 0 0 0 0;
  outline: 0;
}
#department {
  display: flex;
  justify-content: flex-end;
}
#links {
  margin-right: 1rem;
  color: gray;
  text-decoration-color: rgb(41, 175, 70);
}
#logo {
  width: 10rem;
  cursor: pointer;
}
#nav {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0.3rem;
  border: 1px solid rgb(0, 0, 0, 0.1);
}
#footer p {
  float: left;
}
#footer span {
  float: right;
}
#footer {
  height: 20rem;
  background-color: #b9e2fc;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
