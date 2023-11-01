<template>
    <div class="container-fluid fixed-top px-0 wow fadeIn" data-wow-delay="0.1s">
        <div class="top-bar row gx-0 align-items-center d-none d-lg-flex">
            <div class="col-lg-6 px-5 text-start">
            </div>
            <div class="col-lg-6 px-5 text-end">
                <small><i class="fa fa-envelope text-custom-color me-2"></i>enquiries@sahareinsurance.com</small>
                <small class="ms-4"><i class="fa fa-phone-alt text-custom-color me-2"></i>+267 78297630</small>
            </div>
        </div>

        <nav class="navbar navbar-expand-lg navbar-light py-lg-0 px-lg-5 wow fadeIn" data-wow-delay="0.1s">

            <router-link :to="{ name: 'home' }" class="navbar-brand d-flex align-items-center">
                <img class="img-fluid me-3" src="@/assets/img/sahaRelogo.png" alt="" />
            </router-link>
            <button type="button" class="navbar-toggler me-4" data-bs-toggle="collapse" data-bs-target="#navbarCollapse">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarCollapse">
                <div class="navbar-nav ms-auto p-4 p-lg-0">
                    <router-link to="/" class="nav-item nav-link" @click="scrollToTop">Home</router-link>
                    <router-link to="/about" class="nav-item nav-link" @click="scrollToTop">About Us</router-link>
                    <router-link to="/products" class="nav-item nav-link" @click="scrollToTop">Products</router-link>
                    <router-link to="/service" class="nav-item nav-link" @click="scrollToTop">Services</router-link>
                    <router-link :to="{ name: 'contact' }" class="nav-item nav-link" @click="scrollToTop">Contact Us</router-link>
                    <a href="http://blog.sahareinsurance.com/" class="nav-item nav-link" >Media</a>
                </div>
                <div class="d-none d-lg-flex ms-2">
                    <a class="btn btn-light btn-sm-square rounded-circle ms-3" href="https://www.linkedin.com/company/saha-reinsurance-pty-limited/">
                        <small class="fab fa-linkedin-in text-custom-color"></small>
                    </a>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
export default {
  methods: {
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth" 
      });
    }
  }
};
</script>

<style lang="scss" scoped></style>