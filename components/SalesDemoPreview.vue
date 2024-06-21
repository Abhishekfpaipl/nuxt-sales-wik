<template>
    <div class="container">
        <h1 class="text-center py-5 text-capitalize">sales funnel</h1>
        <div class="row m-0 gy-2 mb-4">
            <div class="col-12 col-md-6 align-self-center">
                <img src="~/assets/mobilecontent.svg" style="max-width: 80%; width: 250px;" alt="">
            </div>
            <div class="col-12 col-md-6 g-2 mt-5 mt-md-0">
                <div v-for="(demo, index) in demos" :key="index" class="col">
                    <div class="border-bottom p-1 py-2 m-2">
                        <router-link :to="demo.link"
                            class="d-flex align-items-center justify-content-between text-decoration-none text-dark">
                            <h5 class="text-center mb-0">{{ demo.head }}</h5>

                            <button class="btn btn-danger"> <i class="bi bi-play"></i> Video</button>
                            <button class="btn btn-danger"> <i class="bi bi-eye"></i> Preview</button>
                        </router-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'KycSection',
    data() {
        return {
            demos: [
                {
                    id: 1,
                    head: 'Demo 1',
                    link: '/sales-demo-one'
                },
                {
                    id: 2,
                    head: 'Demo 2',
                    link: '/sales-demo-two'
                },
                {
                    id: 3,
                    head: 'Demo 3',
                    link: '/'
                },
            ],

        }
    },
}
</script>