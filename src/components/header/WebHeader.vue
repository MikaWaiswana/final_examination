<template>
  <header class="shadow-sm container-fluid img1 py-3 border-bottom" style="position: sticky">
    <div class="container-md d-flex justify-content-between align-items-center">
      <!-- Logo -->
      <div class="col-2">
        <div class="logo d-flex align-items-center text-decoration-none">
          <img src="@/assets/img/Logo.svg" alt="foodnow" style="width: 100%;" />
        </div>
      </div>

      <!-- Navigation Toggle for Mobile -->
      <div class="d-lg-none">
        <button
          class="navbar-toggler"
          type="button"
          :class="{ active: isMenuActive }"
          @click="toggleMenu"
          aria-controls="navbarNav"
          :aria-expanded="isMenuActive"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
      </div>

      <!-- Desktop Navigation -->
      <ul class="navigation-bar d-none d-lg-flex list-unstyled my-0">
        <li><a href="#" class="nav-link">Home</a></li>
        <li><a href="#" class="nav-link active">Order</a></li>
        <li><a href="#" class="nav-link">About</a></li>
        <li><a href="#" class="nav-link">Blog</a></li>
        <li><a href="#" class="nav-link">Contact us</a></li>
      </ul>

      <!-- Desktop Signup Menu -->
      <div class="header__signup d-none d-lg-flex fw-semibold justify-content-center align-items-center col-2">
        <a href="#" class="signup-link me-3">Login</a>
        <a href="#" class="signup-link register-link fw-bold px-3 py-1">Register</a>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div class="collapse" :class="{ show: isMenuActive }" id="navbarNav" ref="mobileMenu">
      <ul class="navigation-bar list-unstyled text-center my-3">
        <li><a href="#" class="nav-link">Home</a></li>
        <li><a href="#" class="nav-link active">Order</a></li>
        <li><a href="#" class="nav-link">About</a></li>
        <li><a href="#" class="nav-link">Blog</a></li>
        <li><a href="#" class="nav-link">Contact us</a></li>
      </ul>
      <div class="header__signup fw-semibold d-flex align-items-center justify-content-center">
        <a href="#" class="signup-link">Login</a>
        <a href="#" class="signup-link register-link fw-bold px-3 py-1">Register</a>
      </div>
    </div>

    <!-- Hero Section -->
    <div class="pizza-order-wrapper" :class="{ 'menu-open': isMenuActive }">
      <h1 class="fw-bold display-4">Pizza Order</h1>
    </div>
  </header>
</template>

<script>
export default {
  name: "WebHeader",
  data() {
    return {
      isMenuActive: false, // Menyimpan status toggle menu
    };
  },
  methods: {
    toggleMenu() {
      const menu = this.$refs.mobileMenu;
      if (!this.isMenuActive) {
        // Buka menu dengan transisi halus
        menu.style.height = menu.scrollHeight + "px";
        this.isMenuActive = true;
        setTimeout(() => (menu.style.height = "auto"), 300);
      } else {
        // Tutup menu dengan transisi halus
        menu.style.height = menu.scrollHeight + "px";
        setTimeout(() => (menu.style.height = "0px"), 10);
        this.isMenuActive = false;
      }
    },
  },
};
</script>

<style scoped>
/* General Styling */
.collapse {
  display: block;
  overflow: hidden;
  height: 0;
  transition: height 0.3s ease;
}

.collapse.show {
  height: auto;
}

/* Hero Section Styling */
.pizza-order-wrapper {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #e77e23;
  transition: transform 0.3s ease, padding-top 0.3s ease;
}

.pizza-order-wrapper.menu-open {
  transform: translate(-50%, calc(-50% + 100px));
}

/* Navigation Bar Styling */
.navigation-bar {
  gap: 20px;
  font-weight: 600;
  align-items: center;
}

.nav-link {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #e77e23;
}

.nav-link.active {
  color: #e77e23;
}

/* Signup Menu Styling */
.header__signup {
  gap: 10px;
}

.signup-link {
  text-decoration: none;
  font-size: 1rem;
  transition: color 0.3s ease, background-color 0.3s ease;
  color: #fff;
}

.signup-link:hover {
  color: #e77e23;
}

.register-link {
  background-color: #e77e23;
  color: #fff;
  font-weight: bold;
  text-align: center;
  border-radius: 50px;
}

.register-link:hover {
  background-color: #c16515;
  color: #fff;
}

/* Mobile Styles */
.navbar-toggler {
  border: none;
  background-color: transparent;
  color: #fff;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.navbar-toggler.active {
  background-color: #e77e23;
  color: #fff;
}

.navbar-toggler-icon {
  background-image: url("data:image/svg+xml;charset=UTF8,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 30 30'%3E%3Cpath stroke='rgba%28255,%20255,%20255,%20255%29' stroke-width='2' d='M4 7h22M4 15h22M4 23h22'/%3E%3C/svg%3E");
}

@media (max-width: 768px) {
  .navigation-bar {
    flex-direction: column;
    gap: 10px;
  }

  .header__signup {
    align-items: center;
  }

  .register-link {
    margin-top: 5px;
  }
}
</style>
