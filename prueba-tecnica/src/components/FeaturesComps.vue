<template>
    <div class=" container  ">
        <div class="center-all">
            <h1 class="title is-1">Features designed for you</h1>
            <p>________________________</p>
        </div>
        <br />
        <div class="txt">

            <p class=""> We belive we have created the most efficient SaaS landing page
                for your users. Landing page with features that will convince
                you to use it for your SaaS business.</p>
        </div>
        <div>

            <div class="columns is-multiline is-mobile">
                <div class="column  is-4" v-for="features in feat" :key="features.title" :cols="features.flex">
                    <div class="box">
                        <img src="../assets/responsive-64.png" alt="icon" />
                        <h2 class="title is-5">{{ features.title }}</h2>
                        <br/>
                        <p class="subtitle is-6" v-bind:key="desc.id" v-for="desc in features.description">
                            {{ desc }}
                        </p>
                    </div>
                </div>
            </div>
        </div>

    </div>
</template>

<script>


export default {
    name: 'FeaturesComps',

    data() {
        return {
            feat: [
                {
                    title: "Responsive Layout Template",
                    img: `../assets/responsive-64.png`,
                    description: [
                        "Responsive code that makes your landing page look good on all devices (desktops, tablets, and phones) Created with mobile specialists",
                    ],
                    flex: 4,
                },
                {
                    title: "SaaS Landing Page Analysis",
                    img: `../assets/icons-64-violet/desktop-chart-64.png`,
                    description: [
                        "A perfect structure created after we analized trends in SaaS landing page designs Analysis made to the most popular Saas businesses",
                    ],
                    flex: 4,
                },
                {
                    title: "Smart BEM Grid",
                    img: `../assets/icons-64-violet/browser-64.png`,
                    description: [
                        "Blocks, Elements and Modifiers. A smart HTML/CSS structure that can easely be reused. Layout driven by the purpose of modularity",
                    ],
                    flex: 4,
                },
                {
                    title: "Multiple Unique Designs",
                    img: `../assets/icons-64-violet/desktop-windows-64.png`,
                    description: [
                        "Choose between multiple unique designs and easy integrate elements from one design to another. Following the latest design trends.",
                    ],
                    flex: 4,
                },
                {
                    title: "Flexible HTML Sections",
                    img: `../assets/icons-64-violet/customizer-64.png`,
                    description: [
                        "Simple and Smart HTML code that works reintegrated in any part of the layout. Reuse the elements from one design to another",
                    ],
                    flex: 4,
                },
                {
                    title: "User Friendly",
                    img: `../assets/icons-64-violet/users-64.png`,
                    description: [
                        "Easy to navigate. Made with user experience in mind, in order to provide the perfect landing page experience for your client",
                    ],
                    flex: 4,
                },
            ],
        }
    }
}
</script>

<style>
.center-all {
    align-items: center;
    text-align: center;
    margin-top: 15%;
}

.v-card {
    border: none;
}

.txt {
    padding-left: 15%;
    padding-right: 15%;
    margin-bottom: 5%;
}
</style>

