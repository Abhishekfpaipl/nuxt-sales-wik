<template>
    <div class="">
        <div class="w-100 overflow-auto d-flex align-items-center hide-scroll my-2" ref="slider">
            <div v-for="(review, index) in infiniteReviews" :key="index" @click="showUser(review, index)"
                class="btn m-2 mx-3 d-flex" :class="{ selectedDiv: isSelected(review.id) }">
                <img :src="review.imgr" style="object-fit: contain;" alt="User Image">
            </div>

        </div>

        <div class="shadow container w-100 py-4">
            <p class="text-center fw-bold fs-2 mb-0" style="letter-spacing:6px; text-transform: uppercase;">
                {{ getSelectedReviewInfo.name }}</p>
            <p class="text-center fw-bold fs-4 mb-0" style="text-transform: uppercase; letter-spacing:2px;">
                {{ getSelectedReviewInfo.brand }}</p>
            <p class="text-center" style="letter-spacing:2px;">Member Of</p>
            <p class="text-center fw-bold mb-0 text-secondary" style="letter-spacing:2px; text-transform: uppercase;">
                Post</p>
            <div class="d-flex justify-content-center text-center">
                <p class="w-75 text-secondary" style="font-size: var(--x-small);">{{ getSelectedReviewInfo.text }}</p>
            </div>
            <a class="d-flex justify-content-center w-100 text-decoration-none" :href="getSelectedReviewInfo.url"
                target="_blank">
                <button :href="getSelectedReviewInfo.url" class="btn btn-warning my-3 w-50">Review</button>
                <!-- <button class="btn btn-warning my-3 w-50">{{ getSelectedReviewInfo.btnName }}</button> -->
            </a>

        </div>
    </div>
</template>

<script>
import img1 from "~/assets/11.png"
import img2 from "~/assets/12.webp"
import img3 from "~/assets/13.png"
import img4 from "~/assets/14.png"
import img5 from "~/assets/15.jpg"
import img6 from "~/assets/16.webp"
import img7 from "~/assets/17.jpeg"
import img8 from "~/assets/18.png"
export default {
    data() {
        return {
            selectedReview: 1,
            reviews: [
                {
                    id: 1,
                    show: false,
                    brand: 'Bar Council of India',
                    imgr: img1,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 2,
                    show: false,
                    brand: 'Bharatiya Janta Party',
                    imgr: img2,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 3,
                    show: false,
                    brand: 'Chartered Accountant Of India',
                    imgr: img3,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 4,
                    show: false,
                    brand: 'Cycling Club',
                    imgr: img4,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 5,
                    show: false,
                    brand: 'Delhi Police',
                    imgr: img5,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 6,
                    show: false,
                    brand: 'India Lawers Association',
                    imgr: img6,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 7,
                    show: false,
                    brand: 'International Medical Association',
                    imgr: img7,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 8,
                    show: false,
                    brand: 'National Sports Club Of India',
                    imgr: img8,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 9,
                    show: false,
                    brand: 'Bar Council of India',
                    imgr: img1,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
                {
                    id: 10,
                    show: false,
                    brand: 'Bharatiya Janta Party',
                    imgr: img2,
                    text: ' "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et, impedit."',
                    url: 'https://fpaipl.com/'
                },
            ],
        };
    },
    computed: {

        infiniteReviews() {
            const repeatedReviews = [];
            for (const review of this.reviews) {
                repeatedReviews.push(review);

            }
            return repeatedReviews;
        },
        getSelectedReviewInfo() {
            const selectedReview = this.infiniteReviews[this.selectedReview];
            return {
                text: selectedReview.text,
                name: selectedReview.name,
                brand: selectedReview.brand,
                btnName: selectedReview.btnName,
                url: selectedReview.url
            };
        }
    },

    mounted() {
        this.reviews[this.selectedReview].show = true;
        this.scrollToCenter();
    },
    methods: {
        isSelected(clickedReviewId) {
            return clickedReviewId === this.infiniteReviews[this.selectedReview].id;
        },
        showUser(review, index) {
            this.selectedReview = index;
            this.$store.dispatch('toggleReview', review);
            this.scrollToCenter();
        },
        scrollToCenter() {
            const slider = this.$refs.slider;
            const selectedElement = slider.children[this.selectedReview];
            const scrollLeft =
                selectedElement.offsetLeft - (slider.offsetWidth - selectedElement.offsetWidth) / 1.8;
            slider.scrollLeft = scrollLeft;
        },
    },
};
</script>

<style scoped>
.btn.selectedDiv {
    border: 2px solid #e7e2dc;
}

img {
    width: 80px;
    height: 80px;
}

.btn.selectedDiv img {
    width: 120px !important;
    height: 80px !important;
}

.btn {
    --bs-btn-padding-x: 5px;
    --bs-btn-padding-y: 5px;
}

#style-4 {
    scroll-behavior: smooth;
    overflow-x: scroll;
}

#style-4::-webkit-scrollbar {
    display: none;
}

.hide-scroll {
    overflow-x: hidden;
}

::-webkit-scrollbar {
    width: 10px;
}

::-webkit-scrollbar-track {
    background: #ffffff;
}

::-webkit-scrollbar-thumb {
    background: rgb(134, 132, 132)4f4;
    border-radius: 5px;
    width: 10px;
}

::-webkit-scrollbar-thumb:hover {
    background: #f5e5e5;
    width: 10px;
}
</style>