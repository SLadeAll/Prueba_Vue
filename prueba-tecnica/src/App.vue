<template>
  <div >
    <SearchComp/>
    <div class="container">
        <div>
          <HomeComp/>
          <Features/>
          <TodosMain v-bind:tierList="copyTiers" />
          <FAQComp v-bind:FAQInfo="FAQData"/>
        </div>
    </div>
  </div>
 
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
    
    }
    
      
  },
  created() {
    this.copyTiers = [...this.tiers]
  }
};
</script>
