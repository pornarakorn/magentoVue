<template>
  <div id="app">
    <div class="before_nav">
      <img class="logo" src="img/logo_yellow.png" alt="logo">
      <div class="search">
        <b-nav-form>
          <b-input-group>
            <b-form-input placeholder="Search"></b-form-input>
            <b-input-group-append>
              <b-button variant="success">
                <b-icon icon="search"></b-icon>
              </b-button>
            </b-input-group-append>
          </b-input-group>
          <b-icon icon="cart-3" font-scale="2" class="icon"></b-icon>
        </b-nav-form>
        <b-nav-form class="login">
          <p>Create Account <b-icon icon="person-plus-fill"></b-icon>
          </p>
          <p>Log In <b-icon icon="person-fill"></b-icon>
          </p>
        </b-nav-form>
      </div>
    </div>
    <br>
    <div class="b-nev bar">
      <br><br><br><br>
      <b-navbar toggleable="lg" type="light" class="nav">
        <b-navbar-nav class="nav_text">
          <b-nav-item href="#">Home</b-nav-item>

          <!-- Navbar dropdowns -->
          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown text="User" right>
            <b-dropdown-item href="#">Account</b-dropdown-item>
            <b-dropdown-item href="#">Settings</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-navbar>
    </div>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  #nav {
    padding: 30px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }

  .logo {
    float: left;
    width: 230px;
    height: 100px;
    margin-left: 30px;
    margin-right: 30px;
  }

  .search {
    float: right;
    margin-top: 20px;
  }

  .login {
    float: right;
    margin-top: 20px;
    margin-right: 20px;
    margin-left: 20px;
  }

  .login p {
    margin-left: 20px;
  }

  .icon {
    margin-left: 30px;
    margin-right: 20px;
  }


  .nav {
    background: #c8fdaf;
    margin: 0 auto;
    font-weight: bold;
  }

  .nav_text {
    margin-left: 100px;
  }
</style>