<template>
  <v-app>
    <v-main>
      <SearchComp/>
      <v-contnent>
        <HomeComp/>
        <Features/>
        <TodosMain v-bind:tierList="copyTiers" />
        <FAQComp v-bind:FAQInfo="FAQData"/>
      </v-contnent>
    </v-main>
  </v-app>
</template>

<script>
import TodosMain from './components/TodosMain';
import SearchComp from './components/SearchComp.vue';
import Features from './components/FeaturesComps.vue';
import FAQComp from './components/FAQComp.vue';
import HomeComp from './components/HomeComp.vue';
export default {
  name: 'App',

  components: {
    TodosMain,
    SearchComp,
    HomeComp,
    Features,
    FAQComp,
  },

  data() {
    return {
      tiers: [
      {
        id: 0,
        title: "Free",
        price: "0",
        description: [
          "10 users included",
          "2 GB of storage",
          "Help center access",
          "Email support",
        ],
        buttonText: "Sign up for free",
        buttonVariant: "outlined",
        flex: 3,
      },
      {
        id: 1,
        title: "STARTUP",
        price: "29",
        description: [
          "10 users included",
          "2 GB of storage",
          "Help center access",
          "Email support",
        ],
        buttonText: "Sign up for free",
        buttonVariant: "outlined",
        flex: 3,
      },
      {
        id: 2,
        title: "Pro",
        subheader: "Most popular",
        price: "49",
        description: [
          "20 users included",
          "10 GB of storage",
          "Help center access",
          "Priority email support",
        ],
        buttonText: "Get started",
        buttonVariant: "contained",
        flex: 3,
      },
      {
        id: 3,
        title: "Ultra",
        price: "99",
        description: [
          "50 users included",
          "30 GB of storage",
          "Help center access",
          "Phone & email support",
        ],
        buttonText: "Contact us",
        buttonVariant: "outlined",
        flex: 3,
      },
    ],
    copyTiers: [],
    menuItems: [
          { title: 'Home',  icon: 'home' },
          { title: 'Sign Up',  icon: 'face' },
          { title: 'Sign In', icon: 'lock_open' }
     ],
     FAQData:[
      {
        id: 0,
        question:"Installing the app on all devices",
        desc:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      },
      {
        id: 1,
        question:"How to implement and manage API key",
        desc:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      },
      {
        id: 2,
        question:"How to set up and optimize your account",
        desc:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      },
      {
        id: 3,
        question:"Manage your account access and security settings",
        desc:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      },
      {
        id: 4,
        question:"API integration basic overview",
        desc:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      },
      {
        id: 5,
        question:"Deactivating or deleting your account",
        desc:"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      }
     ]
    }
    
      
  },
  created() {
    this.copyTiers = [...this.tiers]
  }
};
</script>
