﻿<template>
<div>
    <nav class="navbar navbar-toggleable-md navbar-inverse">
        <div class="container">
            <router-link class="navbar-brand" to="/" exact="">
                <i class="fa fa-code" aria-hidden="true"></i>
                VueApp
            </router-link>

            <div class="collapse navbar-collapse">
                <ul class="navbar-nav mr-auto">
                  <router-link tag="li" class="nav-item" to="/" exact>
                    <a class="nav-link">Home</a>
                  </router-link>
                  <router-link tag="li" class="nav-item" to="/view1">
                    <a class="nav-link">View 1</a>
                  </router-link>
                  <router-link tag="li" class="nav-item" to="/view2">
                    <a class="nav-link">View 2</a>
                  </router-link>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container">
        <div class="row" style="margin:10px 0">
            <div id="content">
                <router-view></router-view>
            </div>
        </div>
    </div>

    <h4 style="position: absolute; bottom: 20px; width: 100%; text-align: center">
        <img src="./assets/img/logo.png" />
        <a :href="url">Learn about this Vue VS.NET template</a>
    </h4>
</div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'app-root',
  data() {
    return { url: "https://servicestack.net/vs-templates/VueApp" }
  }
});
</script>
