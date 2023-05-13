<script lang="ts">
import { defineComponent } from 'vue';
import { RouterLink, RouterView } from 'vue-router'
// import HelloWorld from './components/HelloWorld.vue'
export default defineComponent({
  data() {
    return {
      storedTheme: localStorage.getItem('theme')

    }
  },
  methods:
  {

    getPreferredTheme() {
      if (this.storedTheme) {
        return this.storedTheme
      }

      return window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light'
    },

    setTheme(theme: string) {
      if (theme === 'auto' && window.matchMedia('(prefers-color-scheme: dark)').matches) {
        document.documentElement.setAttribute('data-bs-theme', 'dark')
        localStorage.setItem('theme', 'dark');
        this.storedTheme = 'dark';
      } else {
        document.documentElement.setAttribute('data-bs-theme', theme)
        localStorage.setItem('theme', theme);
        this.storedTheme = theme;
      }
    }

  },
  onInit() {
    this.setTheme(this.getPreferredTheme())

  }
})


</script>

<template>
  <header class="container">
    <nav class="navbar navbar-expand-lg bg-indigo rounded" aria-label="Thirteenth navbar example">
      <div class="container-fluid">
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarsExample11"
          aria-controls="navbarsExample11" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse d-lg-flex" id="navbarsExample11">
          <RouterLink to="/" class="navbar-brand col-lg-3 me-0 text-light">Trip Money Tracker</RouterLink>
          <ul class="navbar-nav col-lg-6 justify-content-lg-center">
            <li class="nav-item">
              <RouterLink to="/trips" class="nav-link active text-light">Trips</RouterLink>
            </li>
            <!-- <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle  text-light" href="#" data-bs-toggle="dropdown"
                aria-expanded="false">Dropdown</a>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Trips</a></li>
                <li><a class="dropdown-item" href="#">Another action</a></li>
                <li><a class="dropdown-item" href="#">Something else here</a></li>
              </ul>
            </li> -->
            <li class="nav-item py-2 py-lg-1 col-12 col-lg-auto">
              <div class="vr d-none d-lg-flex h-100 mx-lg-2 text-white"></div>
              <hr class="d-lg-none my-2 text-white-50">
            </li>
            <li class="nav-item dropdown">
              <button class="btn btn-link nav-link py-2 px-0 px-lg-2 dropdown-toggle d-flex align-items-center text-light"
                id="bd-theme" type="button" aria-expanded="false" data-bs-toggle="dropdown" data-bs-display="static"
                aria-label="Toggle theme (light)">
                <i v-if="storedTheme == 'light'" class="bi bi-brightness-high-fill text-light"></i>
                <i v-else class="bi bi-moon-stars-fill text-light"></i>
                <span class="d-lg-none ms-2" id="bd-theme-text">Toggle theme</span>
              </button>
              <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="bd-theme-text">
                <li>
                  <button type="button" class="dropdown-item d-flex align-items-center"
                    :class="{ active: storedTheme == 'light' }" data-bs-theme-value="light" aria-pressed="true"
                    @click="setTheme('light')">
                    <i class="bi bi-brightness-high-fill"></i>
                    Light
                    <i class="bi bi-check2"></i>
                  </button>
                </li>
                <li>
                  <button type="button" class="dropdown-item d-flex align-items-center" data-bs-theme-value="dark"
                    :class="{ active: storedTheme == 'dark' }" aria-pressed="false" @click="setTheme('dark')">
                    <i class="bi bi-moon-stars-fill"></i>
                    Dark
                    <i class="bi bi-check2"></i>
                  </button>
                </li>
              </ul>
            </li>
          </ul>
          <div class="d-lg-flex col-lg-3 justify-content-lg-end">
            <button class="btn btn-success me-2">LogIn</button>
            <button class="btn btn-danger">LogOut</button>
          </div>
        </div>
      </div>
    </nav>
  </header>

  <RouterView />
</template>

<style scoped></style>
