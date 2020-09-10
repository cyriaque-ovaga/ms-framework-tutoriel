<template>
<div>
    <h1>Model</h1>
    <p>
        Les model se trouve dans le dossier
        <strong>app\home\model</strong>, il contient toutes les classes reliés à des tables
    </p>
    <h2>Création d'un model</h2>
    <code>composer new-model $ressource $activity</code>
    <p>Exemple: composer new-model facture pv</p>
    <h2>Configuration du model</h2>
    <p>
        Vous pouvez modifier le nom de table en modifiant la variable
        <strong>$this->table</strong>
        dans la méthode
        <strong>_construct</strong>
    </p>
    <h2>Gestion des champs d'une activité</h2>
    <p>
        Dans la méthode
        <strong>la_bd</strong>, vous pouvez ajouter les champs de votre table.
    </p>
    <code>
        $migration = new \ms\model\migration(new user($serveur));
        <br />$migration->champ("nom", "text");
        <br />$migration->champ("mdp", "text");
        <br />$migration->champ("telephone", "text");
        <br />$migration->champ("sexe", "int");
        <br />$migration->execute();
    </code>
    <h2>Initialiser la base de donnée</h2>
    <p>Pour initialiser la base de donnée en local:</p>
    <code>composer init_bd</code>
    <p>Pour initialiser la base de donnée distant:</p>
    <code>composer init_bd_web</code>
    <h2>Formater un champ à l'entrée</h2>
    <p>
        Vous pouvez faire le contrôle d'une variable avant chargement dans la base de donnée.
        Il suffit de créer une méthode avec le prefixe
        <strong>post_</strong>
    </p>
    <p>
        <strong>Exemple</strong>: Il faudrait que la variable mdp doit être de taille supérieur à 5
    </p>
    <code>
        <br />public function post_mdp($data)
        <br />
        {
        if (strlen($data)
        < 5) { return false; } else { return true; } <br />}
    </code>
    <h2>Formater un champ à la sortie</h2>
    <p>
        Vous pouvez faire le contrôle d'une variable après la requête MySQL.
        Il suffit de créer une méthode avec le prefixe
        <strong>get_</strong>.
    </p>
    <p>
        <strong>Exemple</strong> : Si dans la base de donnée sexe=1 alors un homme sinon une femme dans la variale
        <strong>data_sexe</strong>
    </p>
    <code>
        public function get_sexe($data)
        <br />
        {
        if($data==1){
        return "Homme";
        }else{
        return "Femme";
        }}
        <br />
    </code>
    <h1>Les requêtes MySQL</h1>
    <h2>Recherche</h2>
    <p>Pour faire une recherche simple</p>
    <code>$reponse=$this->app->getmodel("$ressource\$activity")->Select()->Champ('')->Condition('')->exec();</code>
    <p>
        Pour faire une recherche depuis un tableau. Le
        <strong>prefixe</strong> permet peut être
        <strong>vide</strong>
    </p>
    <code>
        $reponse=$this->app->recup->rech($data,"$prefixe");
        <br />$req=$this->app->getmodel("$ressource\$activity")->Select()->Champ("")->Condition($reponse["requete"])->PDO_array($reponse["pdo_array"])->exec();
    </code>
    <p>
        Vous pouvez dans le cadre d'une jointure ajouter la méthode
        <strong>Jointure</strong>
    </p>
    <code>$reponse=$this->app->getmodel("$ressource\$activity")->Select()->Champ('')->Jointure("")->Condition('')->exec();</code>

    <h2>Ajout</h2>
    <p>Pour faire un ajout simple</p>
    <code>$reponse=$this->app->getmodel("$ressource\$activity")->Insert()->Champ(" nom ")->Valeur(" 'test' ")->exec();</code>
    <p>
        Pour faire un ajout depuis un tableau. Le
        <strong>prefixe</strong> permet peut être
        <strong>vide</strong>
    </p>
    <code>
        $reponse= $this->app->recup->add_pdo($data,"$prefixe");
        <br />$last_id = $this->app->getmodel("$ressource\$activity")->Insert()->Champ($reponse['champs'])->Valeur($reponse['valeur'])->PDO_array($reponse['tab'])->exec();
    </code>

    <h2>Modification</h2>
    <p>Pour faire une modification simple</p>
    <code>$this->app->getmodel("$ressource\$activity")->Update()->Valeur(" nom='chouchou' ")->Condition(" id='id' ")->PDO_array()->exec();</code>
    <p>
        Pour faire une modification depuis un tableau. Le
        <strong>prefixe</strong> permet peut être
        <strong>vide</strong>
    </p>
    <code>
        $reponse= $this->app->recup->mod_pdo($data,"$prefixe");
        <br />$this->app->getmodel("$ressource\$activity")->Update()->Valeur($reponse['champs'])->Condition(" id='id' ")->PDO_array($reponse['tab'])->exec();
    </code>

    <h2>Suppression</h2>
    <p>Pour faire une suppression simple</p>
    <code>$this->app->getmodel("$ressource\$activity")->supprimer(array( "valeur"=>" id='$id' ", ));</code>

    <div class="mt-4">
        <nuxt-link to="/controlleur" class="btn btn-primary">Controller -></nuxt-link>
    </div>
</div>
</template>
