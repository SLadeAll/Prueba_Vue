<template>
  <b-navbar>
    <template #start>
      <b-navbar-item href="#">
        Lateral
      </b-navbar-item>

    </template>

    <template #end>
      <b-navbar-item href="#">
        Home
      </b-navbar-item>
      <b-navbar-dropdown label="Features">
        <b-navbar-item href="#">
          About
        </b-navbar-item>
        <b-navbar-item href="#">
          News
        </b-navbar-item>
      </b-navbar-dropdown>
      <b-navbar-item href="#">
        Pricing
      </b-navbar-item>
      <b-navbar-item href="#">
        Contact
      </b-navbar-item>
      <b-navbar-item tag="div">
        <div class="buttons">
          <a class="button ">
           <span> SIGN UP </span>
          </a>
          <a class="button ">
            <span> GET STARTED </span> 
          </a>
        </div>
      </b-navbar-item>
    </template>
  </b-navbar>
</template>
  
<script>
export default {
  name: "SearchComp",
  data: () => ({
    //
  }),
};
</script>

<style>
span {
  color: rgb(138, 43, 226)
}

.btn-space {
  margin-right: 5px;
  margin-left: 5px;
}
</style>