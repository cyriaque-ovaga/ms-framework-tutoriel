<template>
<div>
    <h1>Architecture</h1>
    <h2>vendor</h2>
    <p>Il possède toutes les dépendances COMPOSER;</p>
    <h2>swagger</h2>
    <p>Il contient par défaut tous les codes pour une documentation API.</p>
    <h2>ms</h2>
    <p>Il contient toutes les classes du framework.</p>
    <h3>config</h3>
    <p>Il content la configuration denotre application</p>
    <ul>
        <ul>
            <li>branche : Il permet d'avoir une configuration par branche</li>
            <li>
                app.yaml : Il contient toutes les configurations de votre application
                <ul>
                    <li>hyperlink: Il valide s'il doit utiliser HyperLink</li>
                    <li>middleware: Le middleware par défaut</li>
                </ul>
            </li>
        </ul>
    </ul>
    <h4>controller</h4>
    <p>Il contient tous les codes de traitement des requêtes</p>
    <h4>middleware</h4>
    <p>
        Il s'agit d'une class de controle des informations avant l'envoie dans le
        controlleur
    </p>
    <h4>service</h4>
    <p>
        Une class contenant des services qui seront utilisés pendant votre projet.
    </p>
    <h4>model</h4>
    <p>Il contient les classes qui sont en relation avec nos tables</p>
    <h1>Commande en relation avec architecture</h1>
    <h2>Changer de branche</h2>
    <code>composer branche $nom_branche</code>
    <h2>Accéder à une variable de configuration de l'application</h2>
    <code>$this->app->ma_config["$variable"];</code>
    <div class="mt-4">
        <nuxt-link to="/bd" class="btn btn-primary">Base de données -></nuxt-link>
    </div>
</div>
</template>
