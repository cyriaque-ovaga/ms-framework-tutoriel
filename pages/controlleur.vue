<template>
<div>
    <h1>Controlleur</h1>
    <p>Le controlleur recoit les requetes venant de l'extérieur</p>
    <h2>Création d'un controlleur</h2>
    <code>composer new-controller $ressource $activity</code>
    <p>Exemple: composer new-controller facture pv</p>
    <h3>Transformer les données venant de API en tableau</h3>
    <code>$rep = $this->req_http($data["req"]);</code>
    <h3>Retourner un tableau JSON</h3>
    <code>
        $this->reponse(array(
        "reponse" => true,
        "message" => "",
        "data" => $req
        ));
    </code>
    <div class="mt-4">
        <nuxt-link to="/route" class="btn btn-primary">Route -></nuxt-link>
    </div>
</div>
</template>
