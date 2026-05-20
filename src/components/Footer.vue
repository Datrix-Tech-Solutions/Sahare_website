<template>
    <!-- Footer Start -->
    <div class="container-fluid bg-dark text-light footer mt-5 py-5 wow fadeIn" data-wow-delay="0.1s">
        <div class="container py-5">
            <div class="row g-5">
                <div class="col-lg-3 col-md-6">
                    <div class="mb-4">
                        <img class="img-fluid me-3" src="@/assets/img/sahaRelogo.png" alt="" />
                    </div>
                    <p>
                        Saha Re is a forward-thinking reinsurer dedicated to providing innovative risk management solutions
                        tailored to the evolving insurance landscape.
                    </p>

                </div>

                <div class="col-lg-3 col-md-6">
                    <h4 class="text-white mb-4">Services</h4>
                    <router-link class="btn btn-link" to="/service" @click="scrollToTop">Facultative Reinsurance</router-link>
                    <router-link class="btn btn-link" to="/service" @click="scrollToTop">Treaty Reinsurance</router-link>
                    <router-link class="btn btn-link" to="/service" @click="scrollToTop">Surplus Treaty</router-link>
                    <router-link class="btn btn-link" to="/service" @click="scrollToTop">Special Programs</router-link>
                </div>
                <div class="col-lg-3 col-md-6">
                    <h4 class="text-white mb-4">Quick Links</h4>
                    <router-link :to="{ name: 'about' }" @click="scrollToTop"  class="btn btn-link" >About Us</router-link>
                    <router-link :to="{ name: 'contact' }" @click="scrollToTop" class="btn btn-link">Contact Us</router-link>
                    <router-link :to="{ name: 'service' }" @click="scrollToTop" class="btn btn-link">Our Services</router-link>

                </div>
                <div class="col-lg-3 col-md-6">
                    <h4 class="text-white mb-4">Our Office</h4>
                    <p class="mb-2"><i class="fa fa-map-marker-alt me-3"></i>RDC Tsuma House <br>
                        Plot 50669, Fairground Gaborone, Botswana</p>
                    <p class="mb-2"><i class="fa fa-phone-alt me-3"></i>+267 78297630</p>
                    <p class="mb-2"><i
                            class="fa fa-envelope me-3"></i>enquiries@sahareinsurance.com<br>underwriting@sahareinsurance.com
                    </p>
                    <div class="d-flex pt-2">
                        <!-- <a class="btn btn-square btn-outline-light rounded-circle me-2" href=""><i
                                class="fab fa-twitter"></i></a>
                        <a class="btn btn-square btn-outline-light rounded-circle me-2" href=""><i
                                class="fab fa-facebook-f"></i></a>
                        <a class="btn btn-square btn-outline-light rounded-circle me-2" href=""><i
                                class="fab fa-youtube"></i></a> -->
                        <a class="btn btn-square btn-outline-light rounded-circle me-2" href="https://www.linkedin.com/company/saha-reinsurance-pty-limited/"><i
                                class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Footer End -->


    <!-- Copyright Start -->
    <div class="container-fluid copyright py-4">
        <div class="container">
            <div class="row">
                <div class="col-md-6 text-center text-md-start mb-3 mb-md-0">
                    &copy; <a class="border-bottom" href="#">Saha Re</a>, All Right Reserved.
                </div>
                <div class="col-md-6 text-center text-md-end">
                    <router-link class="border-bottom" :to="{ name: 'privacy' }" @click="scrollToTop">Data Privacy</router-link>
                </div>
            </div>
        </div>
    </div>
    <!-- Copyright End -->
</template>

<script>
export default {
  methods: {
    scrollToTop() {
      // Scroll to the top of the page
      window.scrollTo({
        top: 0,
        behavior: "smooth" // Optional: for smooth scrolling behavior
      });
    }
  }
};
</script>

<style lang="scss" scoped></style>