<template>
  <footer class="container footer" style="background-color: #fdfdfd">
    <hr />
    <div class="container-md">
      <div class="row">
        <!-- Logo dan Sosial Media -->
        <div class="col-md-3">
          <img src="@/assets/img/Logo-alt.svg" alt="" class="mb-2 logo" />
          <p class="mt-4 mb-2 fw-bold fs-5" style="color: #e77e23;">Find Us :</p>
          <div class="fs-4 social-icons">
            <img
              src="@/assets/img/icons/facebook.svg"
              alt=""
              class="p-2 me-3 rounded-circle icon"
            />
            <img
              src="@/assets/img/icons/instagram.svg"
              alt=""
              class="p-2 me-3 rounded-circle icon"
            />
            <img
              src="@/assets/img/icons/youtube.svg"
              alt=""
              class="p-2 me-3 rounded-circle icon"
            />
          </div>
        </div>
        <!-- Navigasi -->
        <div class="col-md-3">
          <h5 class="fw-bold mb-3" style="color: #e77e23;">Navigation</h5>
          <div class="d-flex nav-links">
            <ul class="list-unstyled me-5">
              <li><a href="#" class="text-decoration-none">Home</a></li>
              <li><a href="#" class="text-decoration-none">Order</a></li>
              <li><a href="#" class="text-decoration-none">About</a></li>
              <li><a href="#" class="text-decoration-none">Blog</a></li>
            </ul>
            <ul class="list-unstyled">
              <li><a href="#" class="text-decoration-none">Contact</a></li>
              <li><a href="#" class="text-decoration-none">Login</a></li>
              <li><a href="#" class="text-decoration-none">Register</a></li>
            </ul>
          </div>
        </div>
        <!-- Kontak -->
        <div class="col-md-3">
          <h5 class="fw-bold mb-3" style="color: #e77e23;">Contact</h5>
          <p class="mb-2">
            <img src="@/assets/img/icons/mail.svg" alt="" class="me-2 icon-small" />
            Food.now@mail.com
          </p>
          <p class="mb-2">
            <img src="@/assets/img/icons/phone.svg" alt="" class="me-2 icon-small" />
            +62848477102943
          </p>
          <p>
            <img src="@/assets/img/icons/whatsapp.svg" alt="" class="me-2 icon-small" />
            +628184938494
          </p>
        </div>
        <!-- Lokasi -->
        <div class="col-md-3">
          <h5 class="fw-bold" style="color: #e77e23;">Location</h5>
          <p>
            <img src="@/assets/img/icons/location.svg" alt="" class="icon-small" />
            <span class="fw-bold">Kerobokan</span><br />
            <div class="ms-4" style="margin-top: -15px;">
              <span class="location">Jl. Raya Kerobokan Br Taman, Kuta No.98,<br /></span>
              <span class="location">Kelod, Kec. Kuta Utara,<br /></span>
              <span class="location">Kabupaten Badung, Bali 80361</span>
            </div>
          </p>
        </div>
      </div>
      <hr />
      <!-- Footer bawah -->
      <div class="text-center mt-4">
        <p class="mb-0">
          Copyright © 2022 Foodnow. All Rights Reserved. Powered by PT. Timedoor Indonesia. |
          <a href="#" class="text-decoration-none text-dark">Privacy Policy</a>
        </p>
        <p class="mt-2">
          This site is protected by reCAPTCHA and the Google Privacy Policy and Terms of Service apply.
        </p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
/* Default Styling */
.logo {
  width: 50%;
}

.social-icons .icon {
  border: 1px solid #e77e23;
  transition: all 0.3s ease;
}

.social-icons .icon:hover {
  background-color: #f8d8bd;
}

.icon-small {
  width: 20px;
  margin-right: 8px;
}

/* Links */
a {
  color: #0a0a0a;
  transition: color 0.3s ease;
  font-size: 11px;
}

a:hover {
  color: #e77e23;
}

p {
  font-size: 11px;
}

.location {
  font-size: 11px;
}

/* Responsiveness */
@media (max-width: 768px) {
  .footer .row > div {
    text-align: center;
    margin-bottom: 20px;
  }

  .social-icons {
    justify-content: center;
    display: flex;
  }

  .social-icons .icon {
    margin: 0 5px;
  }
  
  .nav-links {
    justify-content: center;
    text-align: center;
  }

  .nav-links ul {
    margin: 0 auto;
  }
}
</style>
