<template>
<div>
    <h1>DEVOPS</h1>
    <h2>Worflow</h2>
    <p>Nous utilisons un worflow de gestion de projet</p>
    <code>preview -> dev -> stable -> master</code>
    <h3>preview</h3>
    <p>Une branche en libre accès pour le test</p>
    <h3>dev</h3>
    <p>La branche de démarrage de toute prestation</p>
    <h3>stable</h3>
    <p>La branche preprod</p>
    <h3>master</h3>
    <p>La branche de production</p>
    <h2>.gitlab-ci.yml</h2>
    <p>
        Nous proposons un DEVOPS relié à un projet hébergé sur GITLAB et HEROKU
    </p>
    <code>composer gitlab-ci</code>
    <p>
        Pour configurer votre pipeline, vueillez configurer les variables
        d'environnements
    </p>
    <code>
        <br />$HOST_BD = Hostname de la BD <br />$USER_BD = Username de la BD
        <br />$MDP_BD = Mot de passe de la bd <br />$NAME_BD = Nom de la base de
        donnée <br />$HOST_BD_DEV = Hostname de la BD en dévellopemet
        <br />$USER_BD_DEV = Username de la BD en dévellopement <br />$MDP_BD_DEV
        = Mot de passe de la bd en dévellopement <br />$NAME_BD_DEV = Nom de la
        base de donnée en dévellopement <br />$*_url = Les liens vers les
        environnements
    </code>

    <div class="alert alert-info">
        <p align="center">
            Nous sommes à l'attente de toute proposition d'évolution de ces projets
            open-source.
        </p>
    </div>
</div>
</template>
