<template>
    <div class="container d-flex align-items-center w-100" style="padding-top: 70px;">
        <div class="d-flex justify-content-center flex-wrap row">
            <div v-for="(vote, index) in shops" :key="index" class="col-4 col-md-2 position-relative">
                <div class="d-flex justify-content-center text-dark mb-4">
                    <div class="bg-light border rounded-2 d-flex flex-column justify-content-center align-items-center pt-3 px-3 text-dark" style="width: 120px;">
                        <img :src="vote.img" alt="" style="width: 60%;" />
                        <p class="fw-bold my-1 text-center">{{ vote.name }}</p>
                        <div class="d-flex">
                            <small>{{ vote.support }}+</small>
                            &nbsp;
                            <small>Promoters</small>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import img1 from '~/assets/1.png';
import img2 from '~/assets/2.png';
import img3 from '~/assets/3.png';
import img4 from '~/assets/4.png';
import img5 from '~/assets/5.png';

export default {
    data() {
        return {
            shops: [
                { id: 1, img: img1, name: 'Travis', support: 200 },
                { id: 2, img: img2, name: 'Kanye', support: 100 },
                { id: 3, img: img3, name: 'Snoop', support: 200 },
                { id: 4, img: img4, name: 'Weekend', support: 100 },
                { id: 5, img: img5, name: 'Akon', support: 100 },
                { id: 6, img: img1, name: 'Snoop', support: 200 },
                { id: 1, img: img1, name: 'Travis', support: 200 },
                { id: 2, img: img2, name: 'Kanye', support: 100 },
                { id: 3, img: img3, name: 'Snoop', support: 200 },
                { id: 4, img: img4, name: 'Weekend', support: 100 },
                { id: 5, img: img5, name: 'Akon', support: 100 },
                { id: 6, img: img1, name: 'Snoop', support: 200 },
            ],
        };
    }
};
</script>

<style lang="">
</style>
