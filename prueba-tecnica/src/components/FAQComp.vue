<template>
    <div class="Faq">
        <v-row dense>
            <v-col md="6" sm="12">
                <h1>Frequently Asked Questions</h1>
                <p >______</p>

            <h5>
              Have a presale question about our products and features? Or
              looking for a refund? We would love to hear what you concern is.
            </h5>
            <h4>✓ Simple and Smart HTML code</h4>
            <h4>✓ Works reintegrated in any part of the layout</h4>
            <h4>✓ Reuse the elements from one design to another</h4>
            </v-col>
            <v-col md="6" sm="12">
                <v-expansion-panels focusable>
                    <v-expansion-panel v-for="questions in FAQInfo" :key="questions.id">
                        <v-expansion-panel-header>{{ questions.question }}</v-expansion-panel-header>
                        <v-expansion-panel-content>
                            {{ questions.desc }}
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-col>
        </v-row>

    </div>
</template>

<script>
export default {
    props: ['FAQInfo']
}
</script>

<style>
.Faq{
    padding: 10%;
}
</style>