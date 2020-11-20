<template>
<div>
    <h1>Model</h1>
    <p>
        Les model se trouve dans le dossier
        <strong>app\model</strong>, il contient toutes les classes reliés à des
        tables
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
        <strong>champ_table</strong>, vous pouvez ajouter les champs de votre
        table.
    </p>
    <code>
        <br />return array( <br />array( <br />"nom" => "nom", <br />"type" =>
        "text", <br />"description" => "Mon nom", <br />));
    </code>
    <h2>Initialiser la base de donnée</h2>
    <p>Pour initialiser la base de donnée en local:</p>
    <code>composer init_bd</code>
    <p>Pour initialiser la base de donnée distant:</p>
    <code>composer init_bd_web</code>
    <h2>Formater un champ à l'entrée</h2>
    <p>
        Vous pouvez faire le contrôle d'une variable avant chargement dans la base
        de donnée. Il suffit de créer une méthode avec le prefixe
        <strong>post_</strong>
    </p>
    <p>
        <strong>Exemple</strong>: Il faudrait que la variable mdp doit être de
        taille supérieur à 5
    </p>
    <code>
        <br />public function post_mdp($data)
        <br />
        { if (strlen($data)
        < 5) { return false; } else { return true; } <br />}
    </code>
    <h2>Formater un champ à la sortie</h2>
    <p>
        Vous pouvez faire le contrôle d'une variable après la requête MySQL. Il
        suffit de créer une méthode avec le prefixe
        <strong>get_</strong>.
    </p>
    <p>
        <strong>Exemple</strong> : Si dans la base de donnée sexe=1 alors un homme
        sinon une femme dans la variale
        <strong>data_sexe</strong>
    </p>
    <code>
        public function get_sexe($data)
        <br />
        { if($data==1){ return "Homme"; }else{ return "Femme"; }}
        <br />
    </code>
    <h2>Formater avancé</h2>
    <p>
        vous pouvez faire un formatage avancé des données avec la méthode:
        <strong>get_control</strong>.
    </p>
    <h2>Traitement apres initiation de la base de donnée</h2>
    <p>
        Vous pouvez faire une initiation de la base de donnée avec la méthode:
        <strong>after_init_bd</strong>.
    </p>
    <h1>Les requêtes MySQL</h1>
    <p>Vous devez créer la class qui relie votre model:</p>
    <code>$class= new \app\model\$ressource\$activity();</code>
    <h2>Recherche</h2>
    <p>- Pour faire une recherche simple</p>
    <code>$reponse=$class->Select()->Champ('')->Condition('')->exec();</code>
    <p>
        - Pour faire une recherche depuis un tableau. Le
        <strong>prefixe</strong> permet peut être
        <strong>vide</strong>
    </p>
    <code>
        $reponse=$this->app->recup->rech($data,"$prefixe");
        <br />$req=$class->Select()->Champ("")->Condition($reponse["requete"])->PDO_array($reponse["pdo_array"])->exec();
    </code>
    <p>
        - Vous pouvez dans le cadre d'une jointure ajouter la méthode
        <strong>Jointure</strong>
    </p>
    <code>$reponse=$class->Select()->Champ('')->Jointure("")->Condition('')->exec();</code>
    <p>
        - Vous pouvez faire une recherche classique selon un tableau de donnée
    </p>
    <code> $class = new class_model(); <br /></code>
    <code> $req = $class->search($data);</code>

    <h2>Ajout</h2>
    <p>- Pour faire un ajout simple</p>
    <code>$reponse=$class->Insert()->Champ(" nom ")->Valeur(" 'test'
        ")->exec();</code>
    <p>
        - Pour faire un ajout depuis un tableau. Le
        <strong>prefixe</strong> permet peut être
        <strong>vide</strong>
    </p>
    <code>
        $reponse= $this->app->recup->add_pdo($data,"$prefixe");
        <br />$last_id =
        $class->Insert()->Champ($reponse['champs'])->Valeur($reponse['valeur'])->PDO_array($reponse['tab'])->exec();
    </code>
    <p>- Pour faire un ajout depuis un tableau d'une autre manière.</p>
    <code>
        $class->get($array);
        <br />
        $reponse = $class->save();
    </code>

    <h2>Modification</h2>
    <p>- Pour faire une modification simple</p>
    <code>$class->Update()->Valeur(" nom='chouchou' ")->Condition(" id='id'
        ")->PDO_array()->exec();</code>
    <p>
        - Pour faire une modification depuis un tableau. Le
        <strong>prefixe</strong> permet peut être
        <strong>vide</strong>
    </p>
    <code>
        $reponse= $this->app->recup->mod_pdo($data,"$prefixe");
        <br />$class->Update()->Valeur($reponse['champs'])->Condition(" id='id'
        ")->PDO_array($reponse['tab'])->exec();
    </code>

    <p>- Pour faire une modification depuis un tableau d'une autre manière</p>
    <code>
        $class->get($array);
        <br />$reponse = $class->mod(" id='" . $data . "' ","$condition");
    </code>

    <h2>Suppression</h2>
    <p>Pour faire une suppression simple</p>
    <code>$class->supprimer(array( "valeur"=>" id='$id' ", ));</code>
    <p>- Pour une suppression d'une autre manière</p>
    <code> $class->sup(" id='" . $data . "' "); </code>

    <div class="mt-4">
        <nuxt-link to="/controlleur" class="btn btn-primary">Controller -></nuxt-link>
    </div>
</div>
</template>
