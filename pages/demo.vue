<template>
    <div>
        <div class="container py-5">
            <div class="row">
                <div class="col-12 col-md-6 text-center">
                    <h1 class="mb-4 text-capitalize">Book free demo.</h1>
                    <img src="~/assets/demo.svg" class="" style="width:250px; object-fit: contain;" alt="">
                    <div class="d-flex gap-2 justify-content-start align-items-center ps-md-5 text-start text-md-center"
                        v-for="(link, index) in links" :key="index">
                        <i class="bi bi-check text-success fs-4"></i>
                        <p class="my-1">{{ link }}</p>
                    </div>
                </div>
                <div class="col-12 col-md-6 border bg-light p-3 mt-5 mt-md-0">
                    <p class="my-1">Please fill in the form here, and we'll have the best
                        product expert reach out to you for a one-to-one demo.</p>
                    <form @submit.prevent="submitQuery()" class="mt-3 row g-3 needs-validation" novalidate>
                        <div class="w-100 form-floating mb-1">
                            <input type="text" class="form-control" placeholder="" v-model="name" required>
                            <label for="floatingInput" class="text-muted ms-2">Name</label>
                        </div>
                        <div class="w-50 form-floating mb-1">
                            <input type="email" class="form-control" placeholder="Email" v-model="email" required>
                            <label class="ms-2 text-muted">Email</label>
                        </div>
                        <div class="w-50 form-floating mb-1">
                            <input type="tel" class="form-control" placeholder="Mobile" v-model="number" required>
                            <label class="ms-2 text-muted">Mobile No</label>
                        </div>
                        <div class="w-100 form-floating mt-2">
                            <textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea"
                                v-model="note"></textarea>
                            <label for="floatingTextarea" class="ms-2 text-muted">Notes</label>
                        </div>
                        <div class="col-12 mt-5">
                            <button class="btn btn-warning py-2 fs-5 w-100 rounded-0 text-dark" type="submit">Book my
                                free demo</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
        <p class="text-center py-4 text-white mb-0" style="background-color: var(--bg-primary);">Questions? Talk to an
            expert: 886002001</p>
    </div>
</template>
<script>
export default {
    data() {
        return {
            links: [
                "We will get to know first your exact requirements.",
                "Arrange your live and personalized demo of SalesWik.",
                "Explian you how SalesWik can help you to grow your business.",
                "Q&A session with our product expert.",
                "In-depth explanation of pricing and features.",
            ],
            name: "",
            email: "",
            number: "",
            note: "",
        }
    },
    methods: {
        submitQuery() {
            console.log(this.name, this.email, this.number, this.note);
        },
    },
}
</script>
<style lang="">

</style>