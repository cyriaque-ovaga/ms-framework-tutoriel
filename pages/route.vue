<template>
<div>
    <h1>Route</h1>
    <p>
        Les routes se trouvent dans le controlleur au dessus de la méthod
        <strong>app\controller\$ressource\$activity</strong>
    </p>
    <h2>Création d'une route</h2>
    <p>
        Ajouter une méthode dans le controller, mettez en commentaire de
        l'application
    </p>
    <code>
        <br />/** <br />* @route: /$PATH <br />* @method: $METHOD <br />*
        @middleware: $class_middleware <br />* @name: SEARCH $PATH <br />*/
    </code>
    <p>
        <strong>Exemple:</strong>
        <br />
        <code>
            <br />/** <br />* @route: /user/profil <br />* @method: GET <br />*
            @middleware: home <br />* @name: SEARCH user/profil <br />*/
        </code>
    </p>
    <div class="mt-4">
        <nuxt-link to="/swagger" class="btn btn-primary">Swagger -></nuxt-link>
    </div>
</div>
</template>
