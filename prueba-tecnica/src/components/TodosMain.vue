<template>
    <div class="temp text-center">
        <h1 class="">Flexible Pricing</h1>
        <p class="place">We belive we have created the most efficient SaaS landing page  for your users. Landing page with features that will convince you to use it for your SaaS business</p>
        <v-contnet>

        </v-contnet>
        <v-container fluid class="grey lighten-5">
           
            <v-row dense>
                <v-col v-for="tier in tierList" :key="tier.title" :cols="tier.flex" xs="12" sm="12" md="3">
                    <v-card class="text-center  "  elevation="5" outlined tile>
                        <h2 class="ma-2">{{ tier.title }}</h2>
                        <h3 class="ma-2"> {{ tier.price }}$ </h3>
                        <p>Description</p>
                        <ul v-bind:key="desc.id" v-for="desc in tier.description">
                            {{ desc }}
                        </ul>
                        <v-btn color="rgb(138, 43, 226)" elevation="3" large rounded class="ma-2"> <span class="btnText">Sign-Up</span>  </v-btn>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>

    </div>
</template>

<script>

export default {
    name: 'TodosMain',
    comments:{
       
    },

    props: ['tierList']
}
</script>

<style>
    .temp{ padding-left: 15%;
        padding-right: 15%;
    align-items: center; }
    .btnText{
        color: aliceblue;
    }
    .place{
        padding-left: 15%;
        padding-right: 15%;
        margin: 30px;
    }
</style>

