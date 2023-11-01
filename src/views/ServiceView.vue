<template>
    <div>
        <!-- Page Header Start -->
        <div class="container-fluid page-header1 mb-5 wow fadeIn" data-wow-delay="0.1s">
            <div class="container">
                <h1 class="display-3 mb-4 animated slideInDown">Services</h1>
                <nav aria-label="breadcrumb animated slideInDown">
                    <ol class="breadcrumb mb-0">
                        <li class="breadcrumb-item"><a href="#">Home</a></li>
                        <li class="breadcrumb-item active" aria-current="page">Services</li>
                    </ol>
                </nav>
            </div>
        </div>
        <!-- Page Header End -->
        <Services />

        <AddOnServices />

    </div>

</template>

<script setup>
import AddOnServices from '../components/AddOnServices.vue'
</script>

<style lang="scss" scoped></style>