<template>
    <div class="container my-5">
        <h1 class="my-4 text-center text-capitalize">We are offering softwares</h1>
        <div class="row row-cols-1 row-cols-md-3 row-cols-lg-4 g-2">
            <div class="col" v-for="(service, index) in services" :key="index">
                <router-link :to="'/service-sentence/' + service.name" class="card text-decoration-none">
                    <div class="d-flex justify-content-center align-items-center py-2">
                        <div class="border rounded-circle p-3 px-4">{{ index + 1 }}</div>
                    </div>
                    <div class="card-body">
                        <h5 class="card-title text-center text-capitalize">{{ service.name }}</h5>
                        <p class="card-text text-center text-ellipsis">{{ service.description }}</p>
                        <a href="#" class="btn w-100 text-white" style="background-color: var(--bg-primary)">More</a>
                    </div>
                </router-link>
            </div>
        </div>
        <h1 class="my-4 text-center text-capitalize">we are loved by peoples</h1>
        <div class="row row-cols-1 row-cols-md-3 row-cols-lg-4 g-4">
            <div class="col" v-for="(customer, index) in customers" :key="index">
                <router-link :to="'/customer-sentence/' + customer.name" class="card text-decoration-none p-2"
                    :style="{ backgroundColor: customer.color }">
                    <p class="text-center border-bottom py-2 border-dark fs-4"><i class="bi bi-globe"></i></p>
                    <div class="card-body text-center pt-0 ">
                        <p class="card-text text-capitalize my-1 fw-bold">{{ customer.name }}</p>
                        <p class="card-text text-capitalize">Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                            Alias, cupiditate.</p>
                    </div>
                </router-link>
            </div>
        </div>

        <h1 class="my-4 text-center text-capitalize">We are working for Categories</h1>
        <div class="row row-cols-1 row-cols-md-3 row-cols-lg-4 g-4">
            <div class="col" v-for="(category, index) in categories" :key="index">
                <router-link :to="'/category-sentence/' + category" class="card text-decoration-none">
                    <p class="text-center card-header fs-4">
                        <img v-if="category.img" :src="category.img" style="width: 30px;" alt="">
                        <i v-else class="bi bi-globe"></i>
                    </p>
                    <div class="card-body text-center">
                        <p class="card-text text-capitalize my-1 fw-bold">{{ category.name }}</p>
                        <p class="card-text text-capitalize my-1">Lorem ipsum dolor sit amet consectetur adipisicing
                            elit.
                            Alias, quae!</p>
                    </div>
                </router-link>
            </div>
        </div>
        <h1 class="my-4 text-center text-capitalize">our working area</h1>
        <div class="row row-cols-1 row-cols-md-3 row-cols-lg-4 g-2">
            <div class="col" v-for="(place, index) in places" :key="index">
                <router-link :to="'/place-sentence/' + place" class="card text-decoration-none">
                    <p class="text-center card-header text-capitalize border-0">{{ place }}</p>
                </router-link>
            </div>
        </div>
        <img :src="ass" alt="">
    </div>
</template>
<script>
import banner1 from '~/assets/template1.png';
import indus1 from '~/assets/categories/Assembly.svg';
import indus2 from '~/assets/categories/Automobiles.svg';
import indus3 from '~/assets/categories/Boostore.svg';
import indus4 from '~/assets/categories/Business.svg';
import indus5 from '~/assets/categories/Distribution.svg';
import indus6 from '~/assets/categories/Education.svg';
import indus7 from '~/assets/categories/Electronics.svg';
import indus8 from '~/assets/categories/FMCG.svg';
import indus9 from '~/assets/categories/Footwear.svg';
import indus10 from '~/assets/categories/Garments.svg';
import indus11 from '~/assets/categories/Import n Export.svg';
import indus12 from '~/assets/categories/Manufacturing.svg';
import indus13 from '~/assets/categories/Pharmaceuticals.svg';
import indus14 from '~/assets/categories/Restraunts.svg';
import indus15 from '~/assets/categories/Retail Shop.svg';
import indus16 from '~/assets/categories/Retail.svg';
import indus17 from '~/assets/categories/Salon.svg';
import indus18 from '~/assets/categories/Services.svg';
import indus19 from '~/assets/categories/Subscription.svg';
import indus20 from '~/assets/categories/Supermart.svg';
import indus21 from '~/assets/categories/Supply Chain.svg';
import indus22 from '~/assets/categories/Textiles.svg';
import indus23 from '~/assets/categories/Warehouse.svg';
export default {
    name: "MiniFooter",
    data() {
        return {
            servicesList: [

                "Lead Tracking Software", " CRM Software", " Sales Automation Software", " Marketing Automation Software", "Lead Generation Software", "Sales Enablement Software", "Customer Engagement Software",
            ],
            services: [

                // { name: "Product", image: banner1, },
                // { name: "Services", image: banner1, },
                { name: "Lead Tracking", image: banner1, description: "Track and manage leads throughout the sales pipeline efficiently." },
                { name: "CRM", image: banner1, description: "Manage customer relationships, track interactions, and streamline sales processes." },
                { name: "Lead Generation", image: banner1, description: "Generate and capture leads through various online and offline channels." },
                { name: "Sales Enablement", image: banner1, description: "Provide sales teams with tools and content to effectively engage with prospects and close deals." },
                { name: "Sales Automation", image: banner1, description: "Automate repetitive tasks and streamline sales workflows to increase efficiency." },
                { name: "Marketing Automation", image: banner1, description: "Automate marketing processes such as email campaigns, social media, and lead nurturing." },
                { name: "Customer Engagement", image: banner1, description: "Enhance customer interactions and satisfaction through personalized engagement strategies." },
                { name: "Pipeline Management", image: banner1, description: "Efficiently manage and optimize your sales pipeline with our comprehensive pipeline management software." },
            ],
            customers: [
                { name: "agents", color: "#c6def1", },
                { name: "sales person", color: "#f2c6de", },
                { name: "marketing manager", color: "#f7d9c4", },
                { name: "digital marketer", color: "#dbcdf0", },
            ],
            categories: [
                { img: indus1, name: "Assembly" },
                { img: indus2, name: "Automobiles" },
                { img: indus3, name: "Boostore" },
                { img: indus4, name: "Business" },
                { img: indus5, name: "Distribution" },
                { img: indus6, name: "Education" },
                { img: indus7, name: "Electronics" },
                { img: indus8, name: "FMCG" },
                { img: indus9, name: "Footwear" },
                { img: indus10, name: "Garments" },
                { img: indus11, name: "Import n Export" },
                { img: indus12, name: "Manufacturing" },
                { img: indus13, name: "Pharmaceuticals" },
                { img: indus14, name: "Restaurants" },
                { img: indus15, name: "Retail Shop" },
                { img: indus16, name: "Retail" },
                { img: indus17, name: "Salon" },
                { img: indus18, name: "Services" },
                { img: indus19, name: "Subscription" },
                { img: indus20, name: "Supermart" },
                { img: indus21, name: "Supply Chain" },
                { img: indus22, name: "Textiles" },
                { img: indus23, name: "Warehouse" },
                { img: '', name: "Body Massage Centres" },
                { img: '', name: "Cinema Halls" },
                { img: '', name: "Schools" },
                { img: '', name: "Beauty Spas" },
                { img: '', name: "Dermatologists" },
                { img: '', name: "Hospitals" },
                { img: '', name: "Malls" },
                { img: '', name: "Gyms" },
                { img: '', name: "Beauty Parlours" },
                { img: '', name: "Estate Agents" },
                { img: '', name: "Banquet Halls" },
                { img: '', name: "ENT Doctors" },
                { img: '', name: "Book Shops" },
                { img: '', name: "Bike On Rent" },
                { img: '', name: "Sexologist Doctors" },
                { img: '', name: "Neurologists" },
                { img: '', name: "Gynaecologist & Obstetrician Doctors" },
                { img: '', name: "Train Ticket Booking Agents" },
                { img: '', name: "Travel Agents" },
                { img: '', name: "Paying Guest Accommodations" },
                { img: '', name: "General Physician Doctors" },
                { img: '', name: "Dentists" },
                { img: '', name: "Orthopaedic Doctors" },
                { img: '', name: "Chemists" },
                { img: '', name: "Motor Training Schools" },
                { img: '', name: "Gastroenterologists" },
                { img: '', name: "Car Rental" },
                { img: '', name: "Salons" },
                { img: '', name: "Courier Services" },
                { img: '', name: "Dance Classes" },
                { img: '', name: "Pathology Labs" },
                { img: '', name: "Taxi Services" },
                { img: '', name: "Cake Shops" },
                { img: '', name: "AC Repair & Services" },
                { img: '', name: "Mobile Phone Dealers" },
                { img: '', name: "Pet Shops" },
                { img: '', name: "Dmart" },
                { img: '', name: "Packers And Movers" },
                { img: '', name: "Psychiatrists" },
                { img: '', name: "Dharamshalas" },
                { img: '', name: "Urologist Doctors" },
                { img: '', name: "Bakeries" },
                { img: '', name: "Bicycle Dealers" },
                { img: '', name: "Coffee Shops" },
                { img: '', name: "Paediatricians" },
                { img: '', name: "Sonography Centres" },
                { img: '', name: "Yoga Classes" },
                { img: '', name: "Hostels" },
                { img: '', name: "Cardiologists" },
                { img: '', name: "Electrical Shops" },
                { img: '', name: "Skin Care Clinics" },
                { img: '', name: "Diagnostic Centres" },
                { img: '', name: "Homeopathic Doctors" },
                { img: '', name: "Physiotherapists" },
                { img: '', name: "Photo Studios" },
                { img: '', name: "Plumbers" },
                { img: '', name: "Music Classes" },
                { img: '', name: "Electricians" },
                { img: '', name: "Sports Goods Dealers" },
                { img: '', name: "Shoe Dealers" },
                { img: '', name: "Hair Stylists" },
                { img: '', name: "Gift Shops" },
                { img: '', name: "Ophthalmologists" },
                { img: '', name: "Car Repair & Services" },
                { img: '', name: "Ayurvedic Doctors" },
                { img: '', name: "Eye Clinics" },
                { img: '', name: "Restaurants" },
                { img: '', name: "Carpenters" },
                { img: '', name: "Jewellery Showrooms" },
                { img: '', name: "Cooks On Hire" },
                { img: '', name: "Stationery Shops" },
                { img: '', name: "Nephrologists" },
                { img: '', name: "Caterers" },
                { img: '', name: "Interior Designers" },
                { img: '', name: "Rehabilitation Center" },
                { img: '', name: "Grocery Stores" },
                { img: '', name: "Banks" },
                { img: '', name: "ATM" },
                { img: '', name: "5 Star Hotels" },
                { img: '', name: "Hotels" },
                { img: '', name: "Resorts" },
                { img: '', name: "Plastic Surgeons" },
                { img: '', name: "Smart Watch Dealers" },
                { img: '', name: "Drug De Addiction Centres" }
            ],
            places: [
                'Delhi NCR' , 'India'
            ],
        }
    }
}
</script>
<style >
.text-ellipsis {
  display: -webkit-box;
  -webkit-line-clamp: 3;  /* number of lines to show */
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  /* height: calc(1.2em * 3);  1.2em is line height, 3 is number of lines */
}
</style>