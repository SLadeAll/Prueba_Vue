<template>
    <div class="conatiner box-center">
        <div>
            <h1 class="place title is-1">Flexible Pricing</h1>
            <p class="place subtitle ">We belive we have created the most efficient SaaS landing page for your users. Landing page
                with features that will convince you to use it for your SaaS business</p>

            <div class="grey lighten-5">
                <div class="columns is-multiline">
                    <div class="column " v-for="tier in tierList" :key="tier.title" :cols="tier.flex">
                        <div class="box box-center">
                            <h2 class="title">{{ tier.title }}</h2>
                            <h3 class="subtitle"> ${{ tier.price }}/Month </h3>
                            <p>Description</p>
                            <ul v-bind:key="desc.id" v-for="desc in tier.description">
                                {{ desc }}
                            </ul>
                            <b-button type="is-primary" class="but">
                                <strong> <span class="btnText">Sign up</span></strong>
                            </b-button>

                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>

</template>

<script>

export default {
    name: 'TodosMain',
    comments: {

    },

    props: ['tierList']
}
</script>

<style>
.temp {
    padding-left: 15%;
    padding-right: 15%;
}

.btnText {
    color: aliceblue;
}

.place {
    padding-left: 15%;
    padding-right: 15%;
    margin: 10%;
}

.box-center {
    align-items: center;
    text-align: center;
    margin-top: 10%;
    margin-bottom: 10%;
}
.but{
    margin: 5px;
}
span{
    color: white;
}
</style>

