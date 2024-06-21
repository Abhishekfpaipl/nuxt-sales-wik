<template>
    <div style="padding-top: 70px;">
        <div class="text-center fw-bold py-5 text-white" style="background-color: #125252;">
            <p class="fs-1">About Us</p>
            <!-- <p class="fs-5">LOOKING FOR A CAREER, JOIN US !</p> -->
        </div>
        <div class="container py-5 rounded-top-5 bg-white" style="margin-top: -40px;">
            <OurTeam :values="links" /> 
            <div class="my-3">
                <InfoSection :customFields="customFields" />
            </div>
            <div class="my-3">
                <GroupsSection />
            </div>
        </div>

    </div>
</template>
<script>
import img1 from '~/assets/1.png'
import img2 from '~/assets/2.png'
import img3 from '~/assets/3.png'
import img4 from '~/assets/4.png'
import img5 from '~/assets/5.png'
export default {
    name: "AboutUs",
    data() {
        return {
            customFields: [
                {
                    name: "Shop Name",
                    value: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus ."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
                {
                    name: "Description",
                    value: " Lorem ipsum dolor sit amet consectetur adipisicing elit. Ab soluta quis nihil adipisci voluptate impedit placeat aperiam doloremque quasi voluptatibus."
                },
            ],
            links: [
                {
                    id: 1,
                    img: img1,
                    title: "Member 1",
                    description: "Tailored designs to fit your unique brand identity.",
                },
                {
                    id: 2,
                    img: img2,
                    title: "Member 2",
                    description: "Optimized for seamless experiences on all devices.",
                },
                {
                    id: 3,
                    img: img3,
                    title: "Member 3",
                    description: "Efficient CMS solutions for easy content updates.",
                },
                {
                    id: 4,
                    img: img4,
                    title: "Member 4",
                    description: "Robust online stores to boost your sales.",
                },
                {
                    id: 5,
                    img: img5,
                    title: "Member 5",
                    description: "Bespoke applications to meet your business needs.",
                },
            ],
           
        }
    }
}
</script>