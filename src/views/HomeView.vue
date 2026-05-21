<script setup>
import Services from '../components/Services.vue';
import Whyus from '../components/WhyUs.vue'
import AddOnServices from '../components/AddOnServices.vue'
import Classes from '../components/Classes.vue';


</script>

<template>
    <main>

        <!-- Carousel Start -->
        <div class="container-fluid p-0 mb-5 wow fadeIn" data-wow-delay="0.1s">
            <div id="header-carousel" class="carousel slide carousel-fade" data-bs-ride="carousel">
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img class="w-100" src="@/assets/img/home3.png" alt="Image">
                        <div class="carousel-caption">
                            <div class="container">
                                <div class="row justify-content-start">
                                    <div class="col-lg-8">
                                        <p
                                            class="d-inline-block border border-white rounded text-custom-color fw-semi-bold py-1 px-3 animated slideInDown">
                                            Welcome to Saha Re</p>
                                        <h1 class="display-1 mb-4 animated slideInDown">Reinsuring Prosperity
                                        </h1>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="carousel-item">
                        <img class="w-100" src="@/assets/img/home.png" alt="Image">
                        <div class="carousel-caption">
                            <div class="container">
                                <div class="row justify-content-start">
                                    <div class="col-lg-7">
                                        <p
                                            class="d-inline-block border border-white rounded text-custom-color fw-semi-bold py-1 px-3 animated slideInDown">
                                            Welcome to Saha Re</p>
                                        <h1 class="display-1 mb-4 animated slideInDown">Your Trusted Risk Partner</h1>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <button class="carousel-control-prev" type="button" data-bs-target="#header-carousel" data-bs-slide="prev">
                    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Previous</span>
                </button>
                <button class="carousel-control-next" type="button" data-bs-target="#header-carousel" data-bs-slide="next">
                    <span class="carousel-control-next-icon" aria-hidden="true"></span>
                    <span class="visually-hidden">Next</span>
                </button>
            </div>
        </div>
        <!-- Carousel End -->

        <div class="container-fluid py-5 custom-bg">
            <div class="container">
                <div class="row g-0 feature-row">
                    <div class="col-md-6 col-lg-4 text-center wow fadeIn" data-wow-delay="0.1s">
                        <div class="feature-item border  h-100 p-5">
                            <div class="mb-4">
                                <img class="img-fluid" src="@/assets/img/icon/icon-07-light.png" alt="Icon">
                            </div>
                            <h5 class="mb-3">Financial Security</h5>
                            <p class="mb-0 text-white">Financial stability is our hallmark, assuring clients that we can
                                meet our
                                commitments, even in challenging times. We prioritize
                                building enduring relationships and collaborating closely with clients to foster
                                partnerships beyond transactions. </p>
                        </div>
                    </div>
                    <div class="col-md-6 col-lg-4 text-center wow fadeIn" data-wow-delay="0.3s">
                        <div class="feature-item border h-100 p-5">
                            <div class="mb-4">
                                <img class="img-fluid" src="@/assets/img/icon/icon-02-light.png" alt="Icon">
                            </div>
                            <h5 class="mb-3">A Reliable Companion</h5>
                            <p class="mb-0 text-white">In a world fraught with risk, Saha Re is your beacon of
                                trustworthiness and
                                resilience. We empower our partners to thrive in an ever-changing environment, serving as
                                their unwavering risk partner.</p>
                        </div>
                    </div>
                    <div class="col-md-6 col-lg-4 text-center wow fadeIn" data-wow-delay="0.5s">
                        <div class="feature-item border h-100 p-5">
                            <div class="mb-4">
                                <img class="img-fluid icon" src="@/assets/img/icon/technology.png" alt="Icon">
                            </div>

                            <h5 class="mb-3">Innovation Driven Solutions</h5>
                            <p class="mb-0 text-white">In a world marked by growing uncertainty, Saha Re leads in
                                reinsurance
                                innovation, employing advanced data analytics, predictive modeling, and risk assessment
                                tools to empower clients with actionable insights.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Features End -->

        <!-- Features Start -->
        <whyus />
        <!-- Features End -->

        <!-- Service Start -->
        <Services />
        <!-- Service End -->

        <AddOnServices />
        <Classes />

    </main></template>
