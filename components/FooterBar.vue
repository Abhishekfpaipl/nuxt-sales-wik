<template>
    <div class="text-dark bg-light pt-3 border-top border-bottom">

        <div class="d-md-flex flex-column-sm justify-content-evenly py-4 px-3  ">
            <div class="mb-3">
                <router-link to="/">
                    <img :src="img" style="width: 100px;object-fit: contain;">
                </router-link>
                <p class="mb-0 fw-bold fs-2 text-uppercase" style="color: var(--bg-primary)">saleswik</p>
                <p class="mb-2 text-capitalize" style="color: var(--bg-primary);">Empowering Sales, <br> Simplifying Success
                </p>
            </div>
            <div class="mb-3 text-start">
                <p class="mb-2 fw-bold">Contact Us</p>
                <p class="mb-2">Email : support@saleswik.in</p>
                <p class="mb-2">Mob no. : 8860012001</p>
                <p class="mb-2">Address : 2nd Floor, Block B1/632, <br> Janakpuri, 110058, Delhi, India</p>
            </div>
            <div class="mb-3 text-start">
                <p class="mb-2 fw-bold">Reach Us</p>
                <a href="https://www.instagram.com/" class="text-decoration-none text-dark">
                    <p class="mb-2">Instagram</p>
                </a>
                <a href="https://in.linkedin.com/" class="text-decoration-none text-dark">
                    <p class="mb-2">Linkdin</p>
                </a>
                <a href="https://www.facebook.com/" class="text-decoration-none text-dark">
                    <p class="mb-2">Facebook</p>
                </a>
                <a href="https://www.youtube.com/" class="text-decoration-none text-dark">
                    <p class="mb-2">Youtube</p>
                </a>
            </div>
            <div class="mb-3 text-start">
                <p class="mb-2 fw-bold">Resources</p>
                <router-link to="/legal-warning" class="text-dark" style="text-decoration: none;">
                    <p class="mb-2">Legal Warning</p>
                </router-link>
                <router-link to="/privacy-policy" class="text-dark" style="text-decoration: none;">
                    <p class="mb-2">Privacy Policy</p>
                </router-link>
                <router-link to="/term-of-use" class="text-dark" style="text-decoration: none;">
                    <p class="mb-2">Terms Of Use</p>
                </router-link>
                <router-link to="/career" class="text-dark" style="text-decoration: none;">
                    <p class="mb-2">Career</p>
                </router-link>
                <router-link to="/business" class="text-dark" style="text-decoration: none;">
                    <p class="mb-2">Business</p>
                </router-link>
                <router-link to="/reseller-program" class="text-dark" style="text-decoration: none;">
                    <p class="mb-2">Resellership</p>
                </router-link>
            </div>
        </div>
    </div>
    <div class="bg-light text-center py-3 d-flex align-items-center justify-content-center">
        <p class="text-dark mb-0"> Copyright © 2024 sovisor.in All rights reserved</p>
    </div>
</template>

<script>
import logo from '~/assets/logo.svg'
export default {
    name: 'FooterBar',
    data() {
        return {
            img: logo,
        }
    },
}
</script>

<style></style>
