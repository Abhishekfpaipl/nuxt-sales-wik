<template>
  <div class=" " style="padding-top:70px">

    <ServicesFormBanner brandColorOne="#125252" />
    <div class="my-3">
      <ServicesLeadManagement :values="leads" title="Features, that boost your attention!" />
    </div>
    <div class="my-3">
      <BookDemo :faqs="faqs" :image-src="demoImage" title="Book a free demo" image-position="left" />
    </div>
    <div class="my-3">
      <PriceSection />
    </div>
    <div class="my-3">
      <StepsForRegistration />
    </div>
    <div class="my-3">
      <SalesDemoPreview />
    </div>
    <div class="">
      <ImageSection :banner="banner1" brandColorOne="#125252" />
    </div>
    <div class="my-3">
      <SalesFunnel />
    </div>
    <div class="my-3">
      <CustomCounter brandColorOne="#125252" brandTextColor="#78E6B7" name1="customers" :value1="50" name2="years"
        :value2="10" name3="team" :value3="150" />
    </div>
    <div class="my-3">
      <WhyChooseUs :description="whychooseUs" title="why choose us" :image="whyImage" />
    </div>
    <div class="my-3">
      <Comparison />
    </div>
    <div class="my-3">
      <TempFaqs :faqs="faqs" :image-src="faqImage" title="Frequently asked questions" image-position="left" />
    </div>
    <div class="my-3">
      <TempCustomers :reviews="customers" title="our customers" />
    </div>
    <BottomShareIcons />
  </div>
</template>

<script>
import img1 from '~/assets/1.png';
import img2 from '~/assets/2.png';
import img3 from '~/assets/3.png';
import img4 from '~/assets/4.png';
import img5 from '~/assets/5.png';
import banner from '~/assets/banner.jpg';
import banner1 from '~/assets/banner1.png';
import banner2 from '~/assets/banner2.jpg';
import whyImage from '~/assets/whychooseUs.svg';
import faqImage from '~/assets/faq.svg';
import demoImage from '~/assets/demo.svg';
export default {
  data() {
    return {
      banner: banner,
      banner1: banner1,
      banner2: banner2,
      whyImage: whyImage,
      faqImage: faqImage,
      demoImage: demoImage,
      faqs: [
        {
          id: 1,
          question: "What does a CRM system do ?",
          answer: "At its core, the CRM system is designed to manage communications with customers and align all stakeholders involved in interactions with them. However, CRM systems have evolved to perform complex tasks like automating processes, setting up workflows, tracking all conversations and using all the sales and marketing data to derive meaningful reports."
        },
        {
          id: 2,
          question: "Why is CRM important for marketers?",
          answer: "With CRM, marketers can check the performance of their marketing sources, evaluate touchpoints, and more. A CRM helps marketers better understand customers and tune their messaging accordingly. Marketers can also personalize their messages using lead details captured in the CRM platform."
        },
        {
          id: 3,
          question: "What is CRM software used for?",
          answer: "Aligning teams and automating customer-facing processes. Standardizing sales processes and automating them. Managing customer tickets. Tracking the performance of various marketing sources. Reporting and analytics"
        },
        {
          id: 4,
          question: "Why is CRM important in sales?",
          answer: "Because sales reps pursue many leads, CRM plays a significant role in organizing them as per their stages in the sales pipeline. It also helps them keep track of interactions with prospects, schedule meetings, set reminders, and more."
        },
        {
          id: 5,
          question: "How much does a CRM system cost?",
          answer: "Depending on the features, the cost of a CRM system may start from $10-$25 per user per month. CRM companies also offer custom plans for specific features."
        },
      ],
      social: [
        {
          id: 1,
          name: "Instagram",
          url: "http://www.instagram.com/"
        },
        {
          id: 2,
          name: "Facebook",
          url: "http://www.facebook.com/"
        },
        {
          id: 3,
          name: "Linkdin",
          url: "http://in.linkedin.com/"
        },
        {
          id: 4,
          name: "Youtube",
          url: "http://www.youtube.com/"
        },
      ],
      whychooseUs: [
        {
          title: 'Ensure Zero Lead Leakage',
          icon: 'bi-headset'
        },
        {
          title: 'No Missing Follow - ups',
          icon: 'bi-thumbs-up'
        },
        {
          title: "Increase 80 % Additional Sales",
          icon: 'bi-currency-ruppee'
        },
        {
          title: "Cost effective",
          icon: 'bi-journal'
        },
        {
          title: "Secured Plateform",
          icon: 'bi-stars'
        },
        {
          title: "Free support",
          icon: 'bi-stars'
        },
        {
          title: "Modern Interface",
          icon: 'bi-stars'
        },
        {
          title: "Easy Setup & Fast Adoption",
          icon: 'bi-stars'
        },
      ],
      leads: [
        {
          id: 1,
          icon: 'bi-funnel fs-4',
          title: "Lead capture automation",
          description: "Capture leads from all sources- website, facbook, google, lead providers, referrals - onto one platform with zero leakage.",
        },
        {
          id: 2,
          icon: 'bi-diagram-3 fs-4',
          title: "Lead distribution",
          description: "Easily track and distribute leads between your teams based on requirements or other dynamic criteria.",
        },
        {
          id: 3,
          icon: 'bi-hand-thumbs-up fs-4',
          title: "Quality & engagement scoring",
          description: "Auto-qualify leads based on pre-defined rules. Assign scores based on actions they take. Like - website visits, emails opens, link clicks, inquiries, etc",
        },
        {
          id: 4,
          icon: 'bi-megaphone fs-4',
          title: "Sales & marketing automation",
          description: "Automate sales processes. Communicate with leads across various channels - whatsapp, sms, email, phone and more.",
        },
        {
          id: 5,
          icon: 'bi-telephone fs-4',
          title: "Direct Call Integration",
          description: "Call prospects in just one click . Track and record conversations to ensure high compliance and productivity.",
        },
        {
          id: 65,
          icon: 'bi-whatsapp fs-4',
          title: "WhatsApp Call Integration",
          description: "Call prospects in just one click . Track and record conversations to ensure high compliance and productivity.",
        },
        {
          id: 6,
          icon: 'bi-clipboard-data fs-4',
          title: "Real-time dashboards & reports",
          description: "Over 135+ reports help you measure every piece of your process - from campaign spending to sales closure rates.",
        },
        {
          id: 32,
          icon: 'bi-box-arrow-in-down-left fs-4',
          title: "Import Leads",
          description: "Over 135+ reports help you measure every piece of your process - from campaign spending to sales closure rates.",
        },
        {
          id: 43,
          icon: 'bi-box-arrow-up-right fs-4',
          title: "Export Leads",
          description: "Over 135+ reports help you measure every piece of your process - from campaign spending to sales closure rates.",
        },
        {
          id: 13,
          icon: 'bi-stars fs-4',
          image: 'img/features/custom.png',
          title: 'Score leads',
          description: 'Qualify leads based on their region, behavior, and other parameters'
        },
        {
          id: 23,
          icon: 'bi-hand-index fs-4',
          image: 'img/features/gear.png',
          title: 'Assign leads to the right rep',
          description: 'Get the right sales rep on the job based on customer preferences and other predefined criteria.'
        },
        {
          id: 54,
          icon: ' bi-lightning fs-4',
          image: 'img/features/uniform.png',
          title: 'Close deals quickly',
          description: "Generate invoices within CRM from prospect's record and update the deal stage and status."
        },

        {
          id: 72,
          icon: 'bi-archive fs-4',
          title: 'Attach relevant details',
          description: 'Add notes, labels, or other documents to record in CRM.'
        },

        {
          id: 31,
          icon: 'bi-stack-overflow fs-4',
          image: 'img/features/wallet.png',
          title: 'Automate activites',
          description: 'Create workflows for faster, erro-free communication and service.'
        },
        {
          id: 432,
          icon: 'bi-magnet fs-4',
          title: 'lead capture',
          description: 'Get in touch with customers by using our contact form and sync their data with a CRM of your favour.'
        },
        {
          id: 623,
          icon: 'bi-people fs-4',
          title: 'User management',
          description: 'Invite all your team members, upload them by Excel/CSV or connect with Microsoft 365 or google workspace.'
        },
        {
          id: 823,
          icon: ' bi-ui-checks fs-4',
          title: 'Stay connected',
          description: 'Receive real-time notification about activities in CRM across devices.'
        },
        {
          id: 823,
          icon: ' bi-calendar2-date fs-4',
          title: 'Schedule Leads',
          description: 'Receive real-time notification about activities in CRM across devices.'
        },
      ],
      customers: [
        {
          id: 1,
          show: false,
          imgr: img1,
          name: 'Ram',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "We initially thought Saleswik was a small tool that only stores client data but once we started working on it, we knew its depth. We are very excited to use the new features like Team Pipelines, Email-in, and File Cabinet. We 100% recommend Saleswik to everyone!"
        },
        {
          id: 2,
          show: false,
          imgr: img2,
          name: 'Shyam',
          company: 'XYz Pvt Ltd',
          rating: '4.5',
          text: "Saleswik was the perfect solution for our startup, which was moving from paper-based and Excel sheets to an automated solution for sales outreach and managing incoming calls. It has all the basic functionality of other leading CRMs at half the price. In addition, onboarding/training was provided at no additional cost. I highly recommend Zoho Saleswik for any micro business."
        },
        {
          id: 3,
          show: false,
          imgr: img3,
          name: 'Nikhil',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "Loved its UI. I have tried many other apps but this app is the best. The details in which the products are shown in picture is above all."
        },
        {
          id: 4,
          show: false,
          imgr: img4,
          name: 'Abhishek',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "The general idea was to keep everything in one place and at an affordable price, and Saleswik was very accessible that way, and with the ability to expand without switching CRMs."
        },
        {
          id: 5,
          show: false,
          imgr: img5,
          name: 'Rajan',
          company: 'XYz Pvt Ltd',
          rating: '4',
          text: "When you work with software that is structured with features that make it so easy to use—that's when you realize you've struck gold and you don't want to go anywhere else. The pricing is also just right and ideal for small businesses."
        },
        {
          id: 6,
          show: false,
          imgr: img3,
          name: 'Yogesh',
          company: 'XYz Pvt Ltd',
          rating: '4.5',
          text: "Saleswik has been really helpful for us to keep a track on contacts and deals. Since we are small team, Saleswik was so user-friendly that we were able to start using from week 1 of our trial."
        },
        {
          id: 7,
          show: false,
          imgr: img2,
          name: 'Lokesh',
          company: 'XYz Pvt Ltd',
          rating: '4',
          text: "The CRM options available in the market are either too expensive, with complex features that are not essential for a small business, or are priced less with nominal features. But Saleswik is game-changing. It has exceeded our expectations such that V4 Creative cannot work without it."
        },
        {
          id: 8,
          show: false,
          imgr: img1,
          name: 'Bhasker',
          company: 'XYz Pvt Ltd',
          rating: '3.5',
          text: "As vendor and customers needed order visibility, we wanted to automate the entire business and found only Saleswik to be the best suited in terms of integration."
        },
        {
          id: 9,
          show: false,
          imgr: img4,
          name: 'Vivek',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "Saleswik has stayed true to its value proposition—a CRM tailored for small businesses and startups."
        },
        {
          id: 10,
          show: false,
          imgr: img5,
          name: 'Ankit',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "Since the implementation of Saleswik, we have seen positive outcomes in business operations and the accessibility of data. One glance at the Dashboards indicates the performance of my sales folks!"
        },
        {
          id: 11,
          show: false,
          imgr: img2,
          name: 'Karan',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "The mobile app of Saleswik increases productivity on a whole different level. As a small business, it gives us the edge over our competitors and we're very happy to use Saleswik!"
        },
        {
          id: 12,
          show: false,
          imgr: img1,
          name: 'Rajat',
          company: 'XYz Pvt Ltd',
          rating: '4',
          text: "Saleswik helps me stay on track, lets me know where I am at any point of time and what I need to do to reach where I really want to go!"
        },
        {
          id: 13,
          show: false,
          imgr: img4,
          name: 'Ajay',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "Since I started using Saleswik, no lead has been lost. The student conversion rate has increased by 25 percent, to 30 percent."
        },
        {
          id: 14,
          show: false,
          imgr: img2,
          name: 'Vikas',
          company: 'XYz Pvt Ltd',
          rating: '5',
          text: "Saleswik has helped us to decentralize information. Now all the team has access to the documents and sales information. We no longer have the problem that some documents is stored on the PC of a teammate who is not accessible at the time."
        },
      ]
    }
  },
}
</script>