<template>
<div>
    <h1>Installation</h1>
    <p>Le framework MSFRAMEWORK a quelques exigences système.</p>
    <p>
        Vous devrez vous assurer que votre serveur répond aux exigences suivantes
    </p>
    <ul>
        <li>PHP>=7.3</li>
        <li>Extension PHP PDO</li>
        <li>Extension PHP Fileinfo</li>
        <li>Extension PHP PDO</li>
        <li>Extension PHP JSON</li>
    </ul>
    <h2>Installation de MSFramework</h2>
    <p>
        MSFramework utilise Composer pour gérer ses dépendances. Donc, avant
        d'utiliser MSFramework, assurez-vous que Composer est installé sur votre
        machine et GIT.
    </p>
    <code>git clone https://gitlab.com/ms--framework/php-framework.git</code>
    <p>Installer les dépendances :</p>
    <code>composer install</code>
    <p>Pour éxécuter le code :</p>
    <code>php -S localhost:242</code>
    <div class="mt-4">
        <nuxt-link to="/architecture" class="btn btn-primary">Architecture -></nuxt-link>
    </div>
</div>
</template>
