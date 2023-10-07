# [Triade Cybersecurite](https://otardi.gitlab.io/420-313/enjeux/triade/)

On nomme souvent ces trois axes la “triade de cybersécurité”, regroupés sous l’acronyme CIA (de l’anglais Confidentiality, Integrity, Availability).

Cest trois axes sont:
1. La confidentialité
2. L’intégrité
3. La disponibilité



# [Niveaux de risques des évenements](https://otardi.gitlab.io/420-313/enjeux/risque/)

Calculer le rsique d’un évènement permet d’en estimer la gravité, et ainsi de prioriser les mesures de sécurité à prendre.

Deux éléments sont centraux à la notion de risque: la probabilité et l’impact. On représente souvent le calcul du risque avec la formule suivante:

**Risque = (Probabilité d’un évènement) * (Gravité des conséquences)**

Exemple: 
    
- Un évènement assez probable et dont l’impact est important aura un haut niveau de risque. Par exemple, la perte ou le vol d’un disque dur amovible contenant des secrets militaires.

- Un évènement peu probable et dont l’impact est négligeable aura un faible niveau de risque. Par exemple, le fait de deviner le mot de passe de 24 caractères du compte root d’un serveur qui ne contient aucune donnée importante.

- Un évènement rare mais très grave aura environ le même niveau de risque qu’un évènement très probable mais anodin. Par exemple, un incendie dans la salle des serveurs a le même niveau de risque qu’un utilisateur qui oublie son mot de passe.

![alt text](https://otardi.gitlab.io/420-313/images/matrisque2.png)


# [Brevetable](https://otardi.gitlab.io/420-313/pi/types/)

Le but est de donner un avantage temporaire à l’inventeur en évitant qu’il soit en concurrence avec d’autres entreprises.

**Les critères d’une invention brevetable**

1. Être nouvelle: il ne doit pas exister déjà une invention semblable
2. Être utile: elle doit constituer une solution technique à un problème technique
3. Être inventive: elle ne doit pas être évidente pour une personne qui connaît le domaine


**Exemple de brevetable**

- Une méthode d’emballage alimentaire qui prolonge la période de conservation des aliments.
- Une formule chimique pour un une substance qui améliore l’imperméabilité des tissus.
- Une technique permettant de désaliniser l’eau de mer pour la rendre potable.


On ne peut pas breveter n’importe quoi, évidemment: pour des raisons légales ou éthiques, la loi interdit de breveter certaines choses. 

L’objectif est de protéger les vraies inventions, pas de limiter l’utilisation de celles-ci.

**Ainsi il est impossible de déposer une demande de brevet pour les choses suivantes:**

- Une idée ou un concept
- Une théorie scientifique
- Une méthode de traitement médical
- Des formes de vie supérieures (par exemple un être vivant modifié génétiquement)
- Des formes d’énergie
- Des inventions non-techniques ou esthétiques
- Des imprimés

**Exemple de non-brevetable**

- Une pelle pour gauchers. (Une pelle ordinaire est autant utilisable pour les gauchers que le droitiers, donc il n’existe pas de problème technique dont l’invention serait la solution.)
- Une technique de méditation pour améliorer la relaxation. (La relaxation n’est pas un problème technique et n’a pas réellement d’application industrielle.)

# [License](https://otardi.gitlab.io/420-313/pi/licences/)

En Informatique, le copyright n'existe pas, on parle seulement de copyleft.


**Licences copyleft** les 4 libertés, et aussi l’obligation que les versions modifiées d’un logiciel libre soient elles aussi distribuées comme un logiciel libre. Le but est d’éviter une situation où des entreprises copient un logiciel libre, y apportent des modifications et le publient ensuite comme un logiciel commercial, tirant profit du travail bénévole des programmeurs qui l’ont créé à l’origine.

- GPL (GNU General Public License)
- LGPL (GNU Lesser General Public License)
- MPL (Mozilla Public License)

**Licences permissives**
Les licences permissives autorisent de copier, distribuer et modifier le code tout en autorisant que des logiciels propriétaires (non libres) soient créés à partir du code.

- BSD
- MIT
- Apache

**Difference Principal**    

- Lorsqu'on modifie un logiciel copyleft, on est obligé de conserver son nouveau code modifié sous open source afin qu'il puisse être accessible au public.
- Alors que, lorsqu'on modifie un logiciel permissif, il n'y a aucune restriction de ce genre, sauf celle de donner crédit à l'œuvre originale.

# [Clés](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#clés-publiques)

### Clé symétrique
Le terme chiffrement symétrique désigne un système de chiffrement qui utilise **la même clé** pour chiffrer et déchiffrer les messages.

### Clé asymétrique
Les termes chiffrement asymétrique ou chiffrement par clé publique désignent un système de chiffrement qui utilise **des clés différentes** pour chiffrer et déchiffrer les messages.

### *Exemple*

Le chiffrement symétrique, ou chiffrement à clé secrète, utilise une seule clé pour chiffrer et déchiffrer les données. Vous devez partager cette clé avec le destinataire. Disons que vous voulez dire “Je t’aime maman”, que vous écriviez votre e-mail, puis que vous fixiez une clé secrète pour le chiffrer. 

**Lorsque votre maman recevra le message, elle devra entrer la clé secrète pour déchiffrer l’email.**

# [Envoie de message aller-retour avec clé asymétrique](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#authentification)
**Premier message (A vers B) :**

**1 - Génération des paires de clés :** Alice et Bob génèrent chacun leur paire de clés (publique et privée). Alice possède une clé publique et une clé privée, tout comme Bob.

**2 - Chiffrement du premier message :** Alice souhaite envoyer un message à Bob. Elle utilise la clé publique de Bob pour chiffrer le message, de manière à ce que seul Bob puisse le déchiffrer. Le message chiffré est ensuite envoyé à Bob.

**3 - Transfert du premier message chiffré :** Alice envoie le premier message chiffré à Bob par un protocol de communication.

**4 - Déchiffrement du premier message :** Bob utilise sa clé privée pour déchiffrer le premier message qu'il a reçu, ce qui lui permet de lire le contenu du message original.

---

**Deuxième message (B vers A) :**

**1 - Génération des paires de clés :** Les deux parties, Alice et Bob, ont toujours leurs paires de clés générées précédemment.

**2 - Chiffrement du deuxième message :** Cette fois-ci, Bob souhaite envoyer un message à Alice. Il utilise la clé publique d'Alice pour chiffrer son message, de manière à ce que seul Alice puisse le déchiffrer. Le deuxième message chiffré est ensuite envoyé à Alice.

**3 - Transfert du deuxième message chiffré :** Bob envoie le deuxième message chiffré à Alice par un protocol de communication.

**4 - Déchiffrement du deuxième message :** Alice utilise sa clé privée pour déchiffrer le deuxième message qu'elle a reçu, ce qui lui permet de lire le contenu du deuxième message original envoyé par Bob.

# [Encryption avec Linux](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#openssl)
**Créer une clé symétrique (un nombre aléatoire de 128 bits fera l’affaire).**
~~~
openssl rand 128 > cle.bin
~~~

**La syntaxe de la commande enc, qui sert à chiffrer/déchiffrer avec DES, est la suivante:**

`openssl enc -in FICHIER (-out FICHIER) {-e|-d} -CHIFFRE -k CLE (-a)`


~~~
# Pour chiffrer un fichier avec la cle 'cle.bin'
openssl enc -in msgClair.txt -out msgChiffre.bin -e -des3 -k cle.bin

# Pour déchiffrer un fichier avec la cle 'cle.bin'
openssl enc -in msgChiffre.bin -out msgDechiffre.txt -d -des3 -k cle.bin
~~~

**[Chiffrement symétrique avec AES](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#chiffrement-symétrique-avec-aes)**

La commande OpenSSL pour chiffrer/déchiffrer des messages avec AES utilise un mot de passe plutôt qu’une clé numérique. La syntaxe est la suivante:


`openssl CHIFFRE -in FICHIER -out FICHIER -pass:FICHIER{-e|-d} (-a)`

~~~
# Pour chiffrer un fichier avec AES-256 et la clé 'clé.bin'
openssl aes-256-cbc -in msgClair.txt -out msgChiffre.bin -pass file:cle.bin -e 

# Pour déchiffrer un fichier avec la clé 'clé.bin''
openssl aes-256-cbc -in msgChiffre.bin -out msgDechiffre.txt -pass file:cle.bin -d 

~~~
### [Chiffrement par clé publique avec RSA](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#chiffrement-par-clé-publique-avec-rsa)

[**Créer une clé privée**](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#créer-une-clé-privée)

La syntaxe de la commande est la suivante:

`openssl genrsa -out FICHIER TAILLE`
~~~
openssl genrsa -out cle.privee 2048
~~~

[**Créer une clé publique**](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#créer-une-clé-publique)

La syntaxe de la commande pour créer une clé publique est celle-ci:

`openssl rsa -pubout -in FICHIER -out FICHIER`
~~~
openssl rsa -pubout -in cle.privee -out cle.publique
~~~
L’option -pubout signifie qu’on veut que le fichier de sortie soit la clé publique.

[**Chiffrer un message**](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#chiffrer-un-message)

Pour chiffrer un message, on doit spécifier les fichiers d’entrée et de sortie, le fichier de la clé et le fait que celle-ci soit la clé publique:

`openssl pkeyutl -encrypt -inkey FICHIER -pubin -in FICHIER -out FICHIER`
~~~
openssl pkeyutl -encrypt -inkey cle.publique -pubin -in message.txt -out message.bin
~~~

[**Déchiffrer un message**](https://otardi.gitlab.io/420-313/cryptographie1/moderne/#déchiffrer-un-message)

La commande est la suivante:

`openssl pkeyutl -decrypt -inkey FICHIER -in FICHIER -out FICHIER`

~~~
openssl pkeyutl -decrypt -inkey cle.privee -in message.bin -out dechif.txt
~~~

# [X-Correlation-ID](https://http.dev/x-request-id)

Un **X-Correlation-ID** est un en-tête HTTP personnalisé qui est utilisé dans les requêtes et réponses API pour aider à tracer et corréler les requêtes et réponses associées au sein d'un système distribué. Il ne s'agit pas d'un en-tête HTTP standard, mais plutôt d'un exemple d'en-tête personnalisé utilisé à des fins spécifiques.

![alt text](https://global.discourse-cdn.com/auth0/original/3X/c/a/ca69463fc1e605d691fac6b271b97c0d339f71d0.png)

Un **X-Correlation-ID**, bien que n'étant pas une mesure de cybersécurité en soi, peut être un outil utile dans le contexte de la cybersécurité pour diverses raisons:

- **Réponse aux incidents :** en cas d'incident ou de violation de sécurité, disposer d'un identifiant de corrélation peut aider les équipes de sécurité à retracer rapidement les activités et les interactions d'une demande ou d'un utilisateur spécifique sur divers systèmes et services. Ceci est essentiel pour comprendre la portée et l’impact d’un incident de sécurité.
- **Forensics** : lors d’une enquête sur un incident de cybersécurité, il est essentiel de reconstituer la séquence des événements qui ont précédé et suivi l’incident. Les ID de corrélation peuvent aider à reconstruire ces événements en suivant le flux de données et les demandes entre les systèmes.
- **Anomaly Detection:** Security systems and tools often rely on pattern recognition and anomaly detection to identify potential threats. Correlation IDs can be used to group related activities together, making it easier to spot unusual or suspicious patterns of behavior.
- **Surveillance et alertes :** les systèmes de surveillance de la sécurité peuvent utiliser des ID de corrélation pour configurer des alertes pour des modèles d'activité spécifiques. Par exemple, si une série de requêtes avec le même ID de corrélation est détectée comme se comportant de manière anormale, cela peut déclencher une alerte pour une enquête plus approfondie.
- **Débogage et tests** : lors du développement et des tests des fonctionnalités et mécanismes de sécurité, les ID de corrélation peuvent jouer un rôle déterminant dans le traçage du comportement des contrôles de sécurité et l'identification des vulnérabilités ou des erreurs de configuration.

