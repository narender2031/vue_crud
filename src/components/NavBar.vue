<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-brand href="#">Vue demo app</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link to="/" class="nav-link">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/todo" class="nav-link">Todo</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/about" class="nav-link">About</router-link>
            </li>
          </ul>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {};
</script>