<template>

    <div>

        <!-- Page Header Start -->
        <div class="container-fluid page-header mb-5 wow fadeIn" data-wow-delay="0.1s">
            <div class="container">
                <h1 class="display-3 mb-4 animated slideInDown">Contact</h1>
                <nav aria-label="breadcrumb animated slideInDown">
                    <ol class="breadcrumb mb-0">
                        <li class="breadcrumb-item"><a href="#">Home</a></li>
                        <li class="breadcrumb-item active" aria-current="page">Contact</li>
                    </ol>
                </nav>
            </div>
        </div>
        <!-- Page Header End -->

        <!-- Contact Start -->
        <div class="container py-5">
            <div class="container">
                <div class="text-center mx-auto wow fadeInUp" data-wow-delay="0.1s" style="max-width: 500px;">
                    <h1 class="mb-5">If You Have Any Enquiries, Please Contact Us</h1>
                </div>
                <div class="row g-5">
                    <div class="col-lg-6 wow fadeInUp" data-wow-delay="0.1s">

                        <form @submit.prevent="submitForm">

                            <div class="row g-3">
                                <div class="col-md-12">
                                    <div class="form-floating">
                                        <input type="text" v-model="name" class="form-control" id="name"
                                            placeholder="Your Name">
                                        <label for="name">Your Name</label>
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="form-floating">
                                        <input type="email" v-model="email" class="form-control" id="email"
                                            placeholder="Your Email">
                                        <label for="email">Your Email</label>
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="form-floating">
                                        <input type="text" v-model="phone" class="form-control" id="phone"
                                            placeholder="Your Phone Number">
                                        <label for="phone">Your Phone Number</label>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <div class="form-floating">
                                        <input type="text" v-model="subject" class="form-control" id="subject"
                                            placeholder="Subject">
                                        <label for="subject">Subject</label>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <div class="form-floating">
                                        <textarea class="form-control" v-model="message" placeholder="Leave a message here"
                                            id="message" style="height: 200px"></textarea>
                                        <label for="message">Message</label>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <button class="btn custom-bg text-light rounded-pill py-3 px-5" type="submit">Send
                                        Message</button>
                                </div>
                            </div>
                        </form>
                    </div>
                    <div class="col-lg-6 wow fadeInUp" data-wow-delay="0.5s">
                        <h3 class="mb-4">Contact Details</h3>
                        <div class="d-flex border-bottom pb-3 mb-3">
                            <div class="flex-shrink-0 btn-square custom-bg rounded-circle">
                                <i class="fa fa-map-marker-alt text-white"></i>
                            </div>
                            <div class="ms-3">
                                <h6>Our Office</h6>
                                <span>RDC Tsuma House
                                    Plot 50669,<br> Fairground Gaborone, Botswana</span>
                            </div>
                        </div>
                        <div class="d-flex border-bottom pb-3 mb-3">
                            <div class="flex-shrink-0 btn-square custom-bg rounded-circle">
                                <i class="fa fa-phone-alt text-white"></i>
                            </div>
                            <div class="ms-3">
                                <h6>Call Us</h6>
                                <span>+267 78297630</span>
                            </div>
                        </div>
                        <div class="d-flex border-bottom-0 pb-3 mb-3">
                            <div class="flex-shrink-0 btn-square custom-bg rounded-circle">
                                <i class="fa fa-envelope text-white"></i>
                            </div>
                            <div class="ms-3">
                                <h6>Mail Us</h6>
                                <span>enquiries@sahareinsurance.com<br>underwriting@sahareinsurance.com</span>
                            </div>
                        </div>

                        <iframe class="w-100 rounded"
                            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3625.404153676658!2d25.922604875382074!3d-24.678629903587574!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1ebb5be996ffffff%3A0x610e1060d572df99!2sFairgrounds%20Office%20Park!5e0!3m2!1sen!2sgh!4v1697566440087!5m2!1sen!2sgh"
                            width="600" height="350" style="border:0;" allowfullscreen="" loading="lazy"
                            referrerpolicy="no-referrer-when-downgrade"></iframe>
                    </div>
                </div>
            </div>
        </div>
        <!-- Contact End -->
    </div>

</template>

<script setup>
import { ref } from 'vue';
import axios from 'axios';
import Footer from '../components/Footer.vue';
import NavB from '../components/NavB.vue';

const form = ref({
    name: '',
    phone: '',
    email: '',
    subject: '',
    message: ''
});

const name = ref('');
const phone = ref('');
const subject = ref('');
const email = ref('');
const message = ref('');

const submitForm = async () => {
    const formData = {
        recipients: ["underwriting@sahareinsurance.com","enquiries@sahareinsurance.com"],
        sender_email: "info@sahareinsurance.com",
        sender_name: name.value,
        subject: subject.value,
        message: message.value,
        email_smtp_server: "mail.sahareinsurance.com",
        email_smtp_port: 587,
        email_password: "info@2023"
    };

    try {
        const response = await axios.post('http://54.36.167.88:9170/api/v1.0/send-email', formData);
        console.log(response.data);
    } catch (error) {
        console.error(error);
    }
};


</script>

<style lang="scss" scoped></style>