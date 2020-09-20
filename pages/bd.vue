<template>
<div>
    <h1>Base de données</h1>
    <h2>Identifier la branche</h2>
    <p>
        Dans le fichier
        <strong>app\config\app.yaml</strong>, vous pouvez modifier la variable branche
        qui est par défaut
        <strong>master</strong>
    </p>
    <h2>Administrer la base de donnée</h2>
    <p>
        Selon le nom de branche, ouvrir le fichier
        <strong>app\config\branche\master.yaml</strong>.
    </p>
    <p>
        Vous pouvez modifier les variables sachant que celle qui ont un suffixe
        <strong>_dist</strong> correspond à une base de
        donnée distante ou URL distant
    </p>
    <code>
        #Base de donnée local
        <br />db_datatable: "$DATABASE_LOCAL"
        <br />db_hostname: "$HOSTNAME_LOCAL"
        <br />db_username: "$USERNAME_LOCAL"
        <br />db_mdp: "$PASSWORD_LOCAL"
        <br />domain_local: "$URL_LOCAL"
        <br />
        <br />#Base de donnée distant
        <br />db_datatable_dist: "$DATABASE_DIST"
        <br />db_hostname_dist: "$HOSTNAME_DIST"
        <br />db_username_dist: "$USERNAME_DIST"
        <br />db_mdp_dist: "$PASSWORD_DIST"
        <br />domain: "$URL_DIST"
    </code>
    <h2>Créer une la base de donnée local</h2>
    <code>composer create_database</code>
    <h2>Créer une la base de donnée distant</h2>
    <code>composer create_database_web</code>
    <div class="mt-4">
        <nuxt-link to="/model" class="btn btn-primary">Model -></nuxt-link>
    </div>
</div>
</template>
