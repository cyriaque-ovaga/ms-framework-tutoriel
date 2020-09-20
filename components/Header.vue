<template>
<div>
    <nav class="navbar navbar-expand-lg navbar-light bg-dark fixed-top">
        <div class="container">
            <div class="container-fluid">
                <nuxt-link to="/" class="navbar-brand text-white">MSFRAMEWORK</nuxt-link>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav mr-auto mb-2 mb-lg-0">
                        <li class="nav-item">
                            <nuxt-link to="/commencer" class="nav-link text-white">Commencer</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/architecture" class="nav-link text-white">Architecture</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/bd" class="nav-link text-white">Base de données</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/model" class="nav-link text-white">Model</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/controlleur" class="nav-link text-white">Controller</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/route" class="nav-link text-white">Route</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/swagger" class="nav-link text-white">Documentation API</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link to="/devops" class="nav-link text-white">DevOPS</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <a href="https://gitlab.com/ms--framework/" target="_blank" class="btn btn-primary">Gitlab Project</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </nav>
</div>
</template>
