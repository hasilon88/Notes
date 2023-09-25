# [Qu'est ce qu'un hote ?](https://otardi.gitlab.io/420-312/1_hote/1.1_param/)
Un réseau informatique permet de connecter ensemble des ordinateurs « normaux » mais aussi toutes sortes d’autres composants, par exemple des tablettes, consoles de jeu, téléphones, caméras de surveillance, grille-pains…

Le terme hôte est utilisé dans ce contexte pour désigner n’importe quel composant qui a la capacité de se connecter sur un réseau.

![alt](https://www.interviewbit.com/blog/wp-content/uploads/2021/11/IOT.png)

# [Quel système traduit les noms de domaines en adresse ip ?](https://otardi.gitlab.io/420-312/1_hote/1.1_param/#serveur-dns)

***DNS signifie Domain Name System (« Système de noms de domaine »)***

Peu importe qu’un message soit destiné au réseau local ou à internet, pour qu’un message parvienne à destination on doit connaître l’adresse IP de celle-ci. Mais les adresses IP sont utilisées par des machines: lorsqu’on veut ouvrir une page web, on utilise un nom (par exemple collegemv.omnivox.ca); lorsqu’on envoie un courriel on utilise aussi un nom. Mais pour que les hôtes sachent à quelles adresses IP ces noms correspondent, il faut un système de traduction. C’est à cela que servent les serveurs DNS.

![alt](https://cdn.ttgtmedia.com/rms/onlineImages/networking-how_dns_works-f.png)

Dans les petits réseaux comme celui qui est illustré plus haut, c’est souvent la passerelle qui remplit la fonction de serveur DNS. Dans les réseaux de plus grande taille, où les requêtes DNS peuvent être très nombreuses, on consacre un hôte distinct à cette fonction.

**Dans tous les cas, les réseaux ont besoin d’un serveur DNS, et les hôtes d’un réseau ont besoin de savoir quelle est l’adresse de ce serveur DNS pour l’interroger.**

# [Commande Windows qui permet d’afficher les commandes détaillées d’une interface réseau.](https://otardi.gitlab.io/420-312/1_hote/1.2_windows/#informations-réseau)

La commande **`ipconfig`** affiche les paramètres de configuration des interfaces réseau détectées par le système. L’option `/all` affiche des informations détaillées. L’option `/?` permet de voir le manuel d’utilisation de la commande.

Ouvrez un terminal et lancez `ipconfig /all`:

![alt](https://otardi.gitlab.io/420-312/images/ipconfigall.png)

Dans l’exemple précédent il n’y a qu’une seule interface réseau, Ethernet adapter `Ethernet0`.

# [Concentrateur vs commutateur](https://otardi.gitlab.io/420-312/2_connexion_au_reseau/23_concentrateurs_et_commutateurs/)

**Les concentrateurs (hubs) et les commutateurs (switches) sont deux dispositifs utilisés dans les réseaux informatiques pour la connectivité des périphériques, mais ils fonctionnent différemment et ont des caractéristiques distinctes.**

### [Concentrateur](https://otardi.gitlab.io/420-312/2_connexion_au_reseau/2.3_concentrateurs_et_commutateurs/#concentrateur-hub)

Un concentrateur, également appelé hub, est un dispositif réseau de la couche physique (couche 1) du modèle OSI. Son rôle principal est de simplement répéter les données qu’il reçoit d’un port à tous les autres ports sans faire de distinction.

- **Fonctionnement :** Le concentrateur envoie les données reçues sur tous les ports, ce qui signifie que tous les appareils connectés à un concentrateur voient le trafic de tous les autres appareils.

- **Efficacité :** Les concentrateurs ne sont pas efficaces en termes de bande passante, car ils provoquent souvent des collisions de données sur le réseau, ce qui peut entraîner une congestion et des performances médiocres.

- **Sécurité :** Les concentrateurs n’offrent pas de sécurité au niveau du réseau, car tout le trafic est diffusé à tous les appareils.

### [Commutateur](https://otardi.gitlab.io/420-312/2_connexion_au_reseau/2.3_concentrateurs_et_commutateurs/#commutateur-switch)

Un commutateur, également appelé switch, est un dispositif réseau de la couche de liaison de données (couche 2) du modèle OSI. Contrairement aux concentrateurs, les commutateurs sont plus intelligents et prennent des décisions basées sur les adresses MAC (Media Access Control) des périphériques connectés.

- **Fonctionnement :** Les commutateurs examinent l’adresse MAC de chaque trame de données et décident sur quel port la trame doit être envoyée. Cela réduit considérablement le trafic inutile sur le réseau.

- **Efficacité :** Les commutateurs sont beaucoup plus efficaces en termes de bande passante que les concentrateurs, car ils évitent les collisions et optimisent la transmission des données.

- **Sécurité :** Les commutateurs offrent une meilleure sécurité, car ils isolent le trafic entre les ports, limitant ainsi la visibilité du trafic aux appareils autorisés.

### [Differences](https://otardi.gitlab.io/420-312/2_connexion_au_reseau/2.3_concentrateurs_et_commutateurs/#différences)

- **Traitement du trafic :** Les concentrateurs répètent simplement le trafic à tous les ports, tandis que les commutateurs prennent des décisions basées sur les adresses MAC pour acheminer le trafic uniquement vers les ports appropriés.

- **Efficacité :** Les commutateurs sont beaucoup plus efficaces en termes de bande passante, car ils évitent les collisions et minimisent le trafic inutile.

- **Sécurité :** Les commutateurs offrent une meilleure sécurité, car ils isolent le trafic entre les ports, tandis que les concentrateurs diffusent le trafic à tous les appareils.

**En résumé, les commutateurs sont généralement préférés aux concentrateurs dans les réseaux modernes en raison de leur efficacité, de leur capacité à réduire les collisions et de leur meilleure sécurité.**

# [Cable RJ45](https://otardi.gitlab.io/420-312/2_connexion_au_reseau/2.1_types_cables_rj45/)

Il y a plusieurs type de cable RJ45 avec tous des specifications differentes. La liste est la suivante: 

#### 1. Câble Ethernet Catégorie 5e (Cat 5e)
#### 2. Câble Ethernet Catégorie 6 (Cat 6)
#### 3. Câble Ethernet Catégorie 6a (Cat 6a)
#### 4. Câble Ethernet Catégorie 7 (Cat 7)
#### 5. Câble Ethernet Catégorie 8 (Cat 8)
#### 6. Câble Ethernet blindé (screened/foiled twisted pair ou STP/FTP)
#### 7. Câble Ethernet non blindé (unshielded twisted-pair ou UTP)

*Il est essentiel de choisir le type de câble Ethernet approprié en fonction des besoins spécifiques de votre réseau. La catégorie de câble choisie doit correspondre à la vitesse de transmission souhaitée, à la distance à parcourir et à l’environnement d’installation pour garantir des performances optimales de votre réseau.*

### [Câble croisé vs Câble droit](https://choquantecp.medium.com/t568a-vs-t568b-quelle-est-la-diff%C3%A9rence-entre-un-c%C3%A2ble-droit-et-un-c%C3%A2ble-crois%C3%A9-75801beb06b3)

Les termes "câble croisé" (ou "câble crossover") et "câble droit" (ou "câble droit") font référence à deux types de câbles réseau utilisés pour connecter des périphériques tels que des ordinateurs, des commutateurs (switches), des routeurs, etc. 

Ils diffèrent dans la manière dont les fils à l'intérieur du câble sont agencés, ce qui détermine comment les données sont transmises entre les périphériques connectés. 

Voici les différences clés entre les deux :

**Câble droit :**

- Un câble droit est le type de câble réseau le plus couramment utilisé.

- Dans un câble droit, les fils à l'intérieur sont connectés de la même manière aux deux extrémités. Cela signifie que le fil 1 est connecté au fil 1, le fil 2 au fil 2, et ainsi de suite.

- Il est généralement utilisé pour connecter des périphériques différents, tels qu'un ordinateur à un commutateur ou à un routeur, ou un commutateur à un routeur.

**Câble croisé :**

- Un câble croisé est utilisé pour connecter deux périphériques similaires, tels que deux ordinateurs ou deux commutateurs, sans avoir besoin d'un commutateur ou d'un routeur intermédiaire.

- Dans un câble croisé, les fils à l'intérieur sont croisés de telle manière que le fil 1 à une extrémité est connecté au fil 3 à l'autre extrémité, et le fil 2 à une extrémité est connecté au fil 6 à l'autre extrémité. Cette configuration permet aux deux périphériques de communiquer directement entre eux.

- Les câbles croisés étaient couramment utilisés dans le passé, mais de nos jours, de nombreux périphériques modernes, tels que les commutateurs, les routeurs et les ordinateurs, sont capables de détecter automatiquement la configuration du câble et d'ajuster leur communication en conséquence. Par conséquent, les câbles droits sont généralement préférés car ils sont plus polyvalents.

**En résumé, la principale différence entre un câble droit et un câble croisé réside dans la manière dont les fils sont agencés à l'intérieur du câble, ce qui détermine les types de périphériques qu'ils sont destinés à connecter.**

**Les câbles droits sont utilisés pour connecter des périphériques différents, tandis que les câbles croisés sont utilisés pour connecter des périphériques similaires.**

![alt](https://www.conecticplus.com/pub/media/Cable_droit_croise_.png)

# [Système quinaire](https://otardi.gitlab.io/420-312/3_adressage_ip/3.1_binaire/#système-quinaire)

Le système quinaire est un système de numération qui repose sur une base de 5. Contrairement au système décimal (base 10) que nous utilisons couramment, où il y a dix chiffres de 0 à 9, le système quinaire utilise cinq chiffres de 0 à 4 pour représenter les nombres. Chaque position dans un nombre quinaire est une puissance de 5.

Supposons maintenant qu’on dispose de 5 symboles pour compter: 

- △ = 0

- ▽ = 1
- ○ = 2
- ◻ = 3
- ◇ = 4

Pour trouver un nombre en utilisant le système quinaire (base 5) étape par étape, suivez ces étapes simples :

1. Identifiez les symboles quinaires : Tout d'abord, assurez-vous que vous utilisez les symboles quinaires autorisés, tels que △, ▽, ○, ◻, et ◇, pour représenter votre nombre.

2. Affectez une valeur à chaque symbole : Associez une valeur à chaque symbole quinaire selon la correspondance suivante :

    - △ : 0
    - ▽ : 1
    - ○ : 2
    - ◻ : 3
    - ◇ : 4

3. Écrivez votre nombre quinaire : Écrivez votre nombre quinaire en plaçant les symboles de gauche à droite, comme vous le feriez avec les chiffres dans le système décimal. Par exemple, si vous avez le nombre quinaire ○◇△◻, écrivez-le comme cela.

4. Calculez la valeur décimale : Pour convertir votre nombre quinaire en décimal, utilisez la formule suivante :

    Valeur décimale = (Dernier symbole * 5^0) + (Avant-dernier symbole * 5^1) + (Avant-avant-dernier symbole * 5^2) + ...

    Commencez par le dernier symbole (celui le plus à droite) et augmentez les puissances de 5 à mesure que vous avancez vers la gauche.

5. Effectuez les calculs : Pour chaque symbole quinaire, remplacez-le par sa valeur correspondante et effectuez les calculs selon la formule ci-dessus.

6. Additionnez les résultats : Additionnez tous les résultats obtenus pour chaque symbole quinaire après les avoir multipliés par les puissances de 5 appropriées.

7. Le résultat final est la valeur décimale : Une fois que vous avez additionné tous les résultats, vous obtenez la valeur décimale de votre nombre quinaire. C'est le résultat final.

**Par exemple, pour le nombre quinaire ○◇△◻ :**

◻ = 3 * 5^0 = 3

△ = 0 * 5^1 = 0

▽ = 1 * 5^2 = 25

○ = 2 * 5^3 = 250

Additionnez ces valeurs : 3 + 0 + 25 + 250 = 278

Donc, ○◇△◻ en base quinaire est équivalent à 278 en base décimale.

**Sinon, pour convertir de quinaire a decimal, utiliser le script python suivant:**

~~~python
def quinary_to_decimal(quinary_str):
    # Créer un dictionnaire pour mapper les symboles aux chiffres quaternaires
    symbol_to_value = {
        '△': 0,
        '▽': 1,
        '○': 2,
        '◻': 3,
        '◇': 4
    }

    # Renverser la chaîne pour faciliter la conversion
    quinary_str = quinary_str[::-1]

    # Initialiser la valeur décimale à zéro
    decimal_value = 0

    # Parcourir la chaîne et convertir chaque symbole en valeur quinaire
    for i, symbol in enumerate(quinary_str):
        if symbol in symbol_to_value:
            decimal_value += symbol_to_value[symbol] * (5 ** i)
        else:
            print(f"Symbole inconnu trouvé : {symbol}")
            return None

    return decimal_value

# Exemple d'utilisation :
quinary_number = "○◇△◻"
decimal_result = quinary_to_decimal(quinary_number)

if decimal_result is not None:
    print(f"La valeur décimale de {quinary_number} est {decimal_result}")
~~~

# [Trouver réseau a partir d’un masque](https://otardi.gitlab.io/420-312/3_adressage_ip/3.2_adresses_mac_vs_ip/#masque)

Pour trouver le réseau à partir d'un masque de sous-réseau, vous devez également avoir l'adresse IP à laquelle ce masque est associé. Le masque de sous-réseau est utilisé pour diviser une adresse IP en deux parties : la partie réseau et la partie hôte. Voici comment vous pouvez trouver le réseau à partir d'un masque de sous-réseau et d'une adresse IP :

Supposons que vous ayez une adresse IP, par exemple : 192.168.1.10, et un masque de sous-réseau, par exemple : 255.255.255.0 (ou en notation CIDR, /24).

1. Convertissez le masque de sous-réseau en notation binaire :

    255.255.255.0 en binaire est 11111111.11111111.11111111.00000000

2. Appliquez le masque à l'adresse IP en utilisant une opération logique AND bit à bit entre l'adresse IP et le masque de sous-réseau en notation binaire. Cela signifie que chaque bit dans l'adresse IP sera conservé si le bit correspondant dans le masque est à 1, sinon il sera mis à 0.

    Adresse IP : 11000000.10101000.00000001.00001010

    Masque : 11111111.11111111.11111111.00000000 (255.255.255.0 en décimal)

    Résultat : 11000000.10101000.00000001.00000000

3. Convertissez le résultat en notation décimale. Dans cet exemple, le réseau correspondant à l'adresse IP 192.168.1.10 avec un masque de sous-réseau de 255.255.255.0 est 192.168.1.0.

Donc, le réseau correspondant à l'adresse IP 192.168.1.10 avec un masque de sous-réseau de 255.255.255.0 est 192.168.1.0.

**Sinon, utiliser le script python suivant:**

~~~python
# Fonction pour appliquer le masque de sous-réseau en binaire
def apply_subnet_mask(ip_binary, subnet_mask_binary):
    network_address_binary = ""
    for i in range(32):
        network_bit = str(int(ip_binary[i]) & int(subnet_mask_binary[i]))
        network_address_binary += network_bit
    return network_address_binary

# Fonction pour convertir une adresse IP binaire en notation décimale
def binary_ip_to_decimal(binary_ip):
    decimal_ip = ".".join([str(int(binary_ip[i:i+8], 2)) for i in range(0, 32, 8)])
    return decimal_ip

# Adresse IP et masque de sous-réseau en entrée
ip_address = "192.168.2.55"
subnet_mask = "255.255.255.0"

# Convertir l'adresse IP en binaire
ip_binary = "".join([bin(int(octet))[2:].zfill(8) for octet in ip_address.split(".")])

# Convertir le masque de sous-réseau en binaire
subnet_mask_binary = "".join([bin(int(octet))[2:].zfill(8) for octet in subnet_mask.split(".")])

# Appliquer le masque de sous-réseau
network_address_binary = apply_subnet_mask(ip_binary, subnet_mask_binary)

# Convertir le réseau en notation décimale
network_address = binary_ip_to_decimal(network_address_binary)

# Afficher le résultat
print(f"Adresse IP : {ip_address}")
print(f"Masque de sous-réseau : {subnet_mask}")
print(f"Réseau correspondant : {network_address}")
~~~

# [MODÈLE OSI](https://otardi.gitlab.io/420-312/6_pile_tcp-ip/6.2_mod%C3%A8le-osi/)

Le modèle OSI (Open Systems Interconnection) est un cadre conceptuel utilisé pour décrire le fonctionnement des réseaux informatiques et de communication. 

Il divise les processus de communication en sept couches distinctes, chacune ayant des responsabilités spécifiques. Le modèle OSI aide à comprendre comment les différents composants d'un réseau interagissent pour permettre la communication entre les ordinateurs et les appareils. 

Voici une explication simple de chacune des sept couches du modèle OSI :

1. **Couche physique (Physical Layer) :** Cette couche concerne les aspects matériels de la communication, tels que les câbles, les connecteurs et les signaux électriques. Elle détermine comment les bits sont physiquement transmis à travers le réseau.

2. **Couche liaison de données (Data Link Layer) :** Cette couche gère la communication entre des nœuds voisins sur le réseau. Elle gère la détection et la correction des erreurs, ainsi que l'accès au média partagé.

3. **Couche réseau (Network Layer) :** La couche réseau est responsable du routage des données à travers le réseau, en déterminant la meilleure route pour atteindre la destination souhaitée.

4. **Couche transport (Transport Layer) :** Cette couche assure la livraison des données de manière fiable et ordonnée. Elle gère également le contrôle de flux et la segmentation des données en paquets.

5. **Couche session (Session Layer) :** La couche session établit, maintient et termine les sessions de communication entre les applications. Elle gère également la synchronisation et la reprise des données en cas de défaillance.

6. **Couche présentation (Presentation Layer) :** Cette couche s'occupe de la traduction, de la compression et du chiffrement des données pour assurer qu'elles sont correctement interprétées par les applications.

7. **Couche application (Application Layer) :** La couche application est la couche la plus élevée et elle interagit directement avec les applications logicielles. Elle fournit des services de communication et d'interfaçage pour les applications, comme les protocoles de messagerie et de transfert de fichiers.

En résumé, le modèle OSI divise la communication en réseau en différentes étapes logiques, chacune ayant une fonction spécifique. En utilisant ce modèle, les concepteurs de réseaux peuvent mieux comprendre comment les systèmes interagissent pour permettre une communication efficace. 

Il sert également de base pour le développement de protocoles de communication standardisés, tels que le protocole TCP/IP utilisé sur Internet.

![alt](https://otardi.gitlab.io/420-312/images/OSI.png?width=600px)

# [UDP - User Datagram Protocol](https://otardi.gitlab.io/420-312/6_pile_tcp-ip/6.3_ports-tcp-et-udp/#udp---user-datagram-protocol)

Le User Datagram Protocol (UDP) est l'un des principaux protocoles de communication utilisés dans les réseaux informatiques. Il appartient à la couche de transport du modèle OSI et est souvent comparé à un autre protocole de transport largement utilisé, le Transmission Control Protocol (TCP).

Voici quelques caractéristiques importantes du protocole UDP :

1. **Sans connexion :** Contrairement à TCP, qui établit une connexion avant de transférer des données, UDP est un protocole sans connexion. Cela signifie qu'il ne nécessite pas d'établir une session avant de commencer à envoyer des données. Les données sont simplement envoyées de manière autonome, ce qui rend UDP plus rapide mais moins fiable que TCP.

2. **Non fiable :** UDP ne garantit pas la livraison des données ni leur ordre. Il n'y a pas de mécanisme de retransmission intégré, ce qui signifie que si un paquet est perdu en transit, il ne sera pas renvoyé. De plus, les paquets UDP peuvent arriver dans un ordre différent de celui dans lequel ils ont été envoyés.

3. **Communication unicast, broadcast et multicast :** UDP peut être utilisé pour des communications unicast (d'un expéditeur à un destinataire), broadcast (envoi de données à tous les appareils sur un réseau) et multicast (envoi de données à un groupe spécifique d'appareils).

4. **Faible surcharge :** Étant donné qu'UDP n'a pas la surcharge de gestion de la connexion et de la retransmission de paquets associée à TCP, il a moins de latence et de surcharge. Cela le rend approprié pour des applications où une latence minimale est cruciale, telles que les applications de streaming en temps réel, les jeux en ligne et la voix sur IP (VoIP).

5. **Exemples d'utilisation :** UDP est couramment utilisé pour des applications où une légère perte de données est acceptable et où la rapidité de transmission est essentielle. Cela inclut des services tels que DNS (Domain Name System), SNMP (Simple Network Management Protocol), des flux vidéo en temps réel, des applications de jeux en ligne, etc.

***En résumé, UDP est un protocole de communication rapide, sans connexion et moins fiable que TCP. Il est adapté à des applications où la vitesse est essentielle et où une légère perte de données est acceptable, mais il ne convient pas aux applications qui nécessitent une transmission fiable et garantie des données.***

***Essentiellement il ne sert que de transition entre la couche IP et et la couche d’application.***

![alt](https://www.atatus.com/blog/content/images/2022/07/udp-vs-tcp--1-.png)

# [Qu'est-ce qu'un réseau de l'informatique ?](https://aws.amazon.com/fr/what-is/computer-networking/#:~:text=Le%20r%C3%A9seau%20informatique%20d%C3%A9signe%20les,technologies%20physiques%20ou%20sans%20fil.)

Le réseau informatique désigne les appareils informatiques interconnectés qui peuvent échanger des données et partager des ressources entre eux. Ces appareils en réseau utilisent un système de règles, appelées protocoles de communication, pour transmettre des informations sur des technologies physiques ou sans fil.

![alt](https://cours-informatique-gratuit.fr/wp-content/uploads/2014/05/brancher-internet.jpg)

# [Topologie réseau](https://web.maths.unsw.edu.au/~lafaye/CCM/initiation/topologi.htm#:~:text=La%20topologie%20logique%2C%20par%20opposition,Ethernet%2C%20Token%20Ring%20et%20FDDI.)

Un réseau informatique est constitué d'ordinateurs reliés entre eux grâce à des lignes de communication (câbles réseaux, etc.) et des éléments matériels (cartes réseau, ainsi que d'autres équipements permettant d'assurer la bonne circulation des données). L'arrangement physique, c'est-à-dire la configuration spatiale du réseau est appelé topologie physique. 

On distingue généralement les topologies suivantes :

- Réseau en étoile
- Réseau en bus
- Réseau en anneau
- Réseau maillé
- Réseau en arbre (ou hiérarchique)

La topologie logique, par opposition à la topologie physique, représente la façon dont les données transitent dans les lignes de communication. Les topologies logiques les plus courantes sont Ethernet, Token Ring et FDDI.

![alt](https://www.aquaportail.com/pictures2203/topologie-de-reseau.jpg)
