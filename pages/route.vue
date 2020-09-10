<template>
<div>
    <h1>Route</h1>
    <p>
        Les routes se trouvent dans le fichier
        <strong>app\home\assets\config\route_public.yaml</strong>
    </p>
    <h2>Création d'une route</h2>
    <code>
        $NAME_URL:
        <br />Path: /$PATH/(?'req'[^/]+)
        <br />Ctr: 'app\home\controller\$ressource\$activity::$method'
    </code>
    <p>
        <strong>Exemple:</strong>
        <br />
        <code>
            Homes:
            <br />Path: /user/user/delete/(?'req'[^/]+)
            <br />Ctr: 'app\home\controller\user\user::delete'
        </code>
    </p>
    <p>
        Le
        <strong>$PATH</strong> montre le lien qui qui appel la requête,
        <strong>app\home\controller\$ressource\$activity</strong>
        est le lien vers le controlleur et
        <strong>$method</strong> la méthode qui sera utilisé.
    </p>
    <h2>Création d'une api</h2>
    <p>
        Vous pouvez faire un crundle API d'une table. Il va le code dans
        <strong>route_public.yaml</strong>
    </p>
    <code>composer makeapi $ressource $method</code>
</div>
</template>
