# 🛡️ Security Questions and Solutions

### 1. 🔒 Fail2ban Configuration
**Question:** Vous souhaitez faire en sorte que fail2ban bloque pour une heure toutes les adresses IP (sauf **192.168.23.21**) lorsqu’il y a 4 tentatives de connexions erronées en 12 minutes. Comment faites-vous? Expliquez la procédure.

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
1. Ouvrez ou créez un fichier dans /etc/fail2ban/jail.d/. Par exemple, vous pouvez nommer ce fichier defaults-debian.local.

2. Ajoutez ou modifiez les configurations suivantes :

    [DEFAULT]
    ignoreip = 127.0.0.1/8 192.168.23.21
    findtime = 720  # 12 minutes en secondes
    bantime = 3600  # 1 heure en secondes
    maxretry = 4

    [sshd]
    enabled = true


```
</p>
</details>

---

### 2. 🐉 Hydra: Attaque ou Défense?
**Question:** Le programme hydra est-il un moyen d’attaque ou de défense? Expliquez brièvement votre réponse.

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
Hydra est un moyen d'attaque car il permet de crack des mots de passes.
```

</p>
</details>

---

### 3. 🖥️ Utilisation de Hydra
**Question:** Comment devez-vous appeler hydra pour qu’il s’exécute avec les options suivantes :
- Connexion par SSH à destination de **10.100.23.78**
- 1 connexion toutes les 2 secondes
- La liste des utilisateurs est dans le fichier util.txt
- Les mots de passe sont dans le fichier mots.txt

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
hydra -L util.txt -P mots.txt 10.100.23.78 ssh
```

</p>
</details>

---

### 4. 🛡️ Fail2ban: Attaque ou Défense?
**Question:** Le programme fail2ban est-il un moyen d’attaque ou de défense? Expliquez brièvement votre réponse.

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
Fail2ban est un outil de défense car il permet de blocker des addresses IP suspects.
```

</p>
</details>

---

### 5. 💉 SQL Injection et le caractère '#'
**Question:** Dans une page vulnérable aux injections SQL, on a le formulaire suivant:

![alt](https://www.w3resource.com/w3r_images/secure-form.png)

Dans le champ « User ID » on entre le texte suivant : 
    
```sql
' or 1=1; #
```

Expliquez à quoi sert le « `#` » ici, et ce qui se passerait s’il était absent.

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
Permet d'ignorer le reste de la requête puisque ça met le reste en commentaire. Cela prévient des erreurs de syntaxes ou d'autres problèmes.
```

</p>
</details>

---

### 6. 🗃️ Erreur de Requête SQL
**Question:** Expliquez pourquoi la requête suivante cause une erreur :
`SELECT 1,2,3 UNION SELECT 4,5,6,7`

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
Parce qu'il faut que les deux requêtes ont le meme nombre de colonnes.
```
</p>
</details>

---

### 7. 🌐 Injection de Script et Échappement de Caractères
**Question:** Vous tentez d’injecter le code `<script>alert(1)</script>` dans une page et vous constatez que la source contient ceci: 

```html
&lt;script&gt;alert(1)&lt;/script&gt;
```

Expliquez ce que vous pouvez en conclure.

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
On performe une attaque de type `XSS basée sur le DOM` car elle modifie le `DOM` du code `HTML` correspendant. Donc, ce type d'injection en fonctionne pas car il n'est pas possible d'injecter dans du code `HTML`.
```
</p>
</details>

---

### 8. 📊 MySQL: Requête pour Noms de Colonnes
**Question:** Sur une base de données de type MySQL, quelle requête peut-on faire pour obtenir le nom de toutes les colonnes d’une table nommée « produits »?

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```sql
SELECT column_name FROM information_schema.COLUMNS WHERE table_name='produits';
```

</p>
</details>

---

### 9. 🕵️‍♂️ Types de XSS
**Question:** Il y a 3 types de XSS : 
- `les XSS réfléchies`
- `les XSS stockées`
- `les XSS basées sur le DOM` 

Quel type de XSS a pour effet de modifier le contenu de la BD qui contient les données du site?

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
Les XSS stockées car c'est dans la base de donnée que le code javascript malveillant est stocké.
```
</p>
</details>

---

### 10. 🌐 XSS dans un Champ de Recherche
**Question:** Vous constatez que le texte entré dans un champ de recherche apparaît comme valeur d’un attribut dans la page des résultats de recherche. 
Par exemple, si vous recherchez le terme « souris », la page qui affiche les résultats contient l’élément suivant :

```html
<div id='keyword' value='souris'>souris</div>
```

Vous exploitez cette vulnérabilité en entrant le terme suivant dans le champ de recherche :
```html
'><script>alert(1)</script>
```

Dans le code source de la page des résultats, vous voyez donc cet élément :
```html
<div id='keyword' value=''><script>alert(1)</script>'>
```

Quel est le type de cette `XSS (stockée, réfléchie, basée sur le DOM)`? Expliquez brièvement votre réponse.

<details>
<summary><b>🔑 Solution</b></summary>
<p>

```
XSS stockée car le code est stockée est dans la base de donnée.
```

</p>
</details>

---
