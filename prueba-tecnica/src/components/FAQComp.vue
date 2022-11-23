<template>
    <div class="container">
        <div class="columns is-multiline">
            <div class="column is-half">
                <div class="box">
                    <h1 class="title is-4">Frequently Asked Questions</h1>

                    <h5>
                        Have a presale question about our products and features? Or looking
                        for a refund? We would love to hear what you concern is.
                    </h5>
                    <h4>✓ Simple and Smart HTML code</h4>
                    <h4>✓ Works reintegrated in any part of the layout</h4>
                    <h4>✓ Reuse the elements from one design to another</h4>
                </div>
            </div>
            <div class="column is-half">
                <div id="app" class="container">
                    <section>
                        <b-collapse class="card" animation="slide" v-for="(collapse, index) of collapses" :key="index"
                            :open="isOpen == index" @open="isOpen = index" :aria-id="'contentIdForA11y5-' + index">
                            <template #trigger="props">
                                <div class="card-header" role="button" :aria-controls="'contentIdForA11y5-' + index"
                                    :aria-expanded="props.open">
                                    <p class="card-header-title">
                                        {{ collapse.title }}
                                    </p>
                                    <a class="card-header-icon">
                                        <b-icon :icon="props.open ? 'menu-down' : 'menu-up'">
                                        </b-icon>
                                    </a>
                                </div>
                            </template>
                            <div class="card-content">
                                <div class="content">
                                    {{ collapse.text }}
                                </div>
                            </div>
                        </b-collapse>
                    </section>
                </div>

                <!-- <v-expansion-panels focusable>
                    <v-expansion-panel v-for="questions in FAQInfo" :key="questions.id">
                        <v-expansion-panel-header>{{
                                questions.question
                        }}</v-expansion-panel-header>
                        <v-expansion-panel-content>
                            {{ questions.desc }}
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ["FAQInfo"],
    data() {
        return {
            isOpen: 0,
            collapses: [
                {
                    id: 0,
                    title: "Installing the app on all devices",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                },
                {
                    id: 1,
                    title: "How to implement and manage API key",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                },
                {
                    id: 2,
                    title: "How to set up and optimize your account",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                },
                {
                    id: 3,
                    title: "Manage your account access and security settings",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                },
                {
                    id: 4,
                    title: "API integration basic overview",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                },
                {
                    id: 5,
                    title: "Deactivating or deleting your account",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
                }

            ]
        };
    },
};
</script>

<style>

</style>
