

Alertes leboncoin.fr - 4.1.6
=============================
Recevez par email vos recherches leboncoin.fr (via Google Sheets / App Script)

<div style="float:right;"><img src="https://raw.githubusercontent.com/maximelebreton/alertes-leboncoin/master/main.png"/></div>
_____________________________


**Prérequis :** *vous devez avoir un compte Google et y être connecté.*

Installation en 4 étapes
----------------------------------
1. **Créez une copie** de cette feuille de calcul : https://docs.google.com/spreadsheet/ccc?key=1oruKJqdbEjg0z28K83hsqIKbaL2weBMqmA8lG0gYIfw&newcopy
 
2. **Renseignez votre adresse email** dans l'onglet `Variables` en bas du document

3. Pour que le script soit executé de manière automatique, vous devez **programmer un trigger*** sur la fonction alertesLeBonCoin().  
(Dans outils > editeur de scripts, puis `Ressources > Déclencheurs du script actuel`).  
<small>* *il est vivement conseillé de ne pas aller en dessous de `toutes les 2 heures`.*</small>

4. Pour chaque requête que vous souhaitez effectuer sur leboncoin.fr, **copiez/collez son url** dans la colonne `Url` (une url par ligne). 

5. **Voilà !** Vous pouvez faire un test en cliquant sur `Alertes LeBonCoin > Lancer manuellement`. (une autorisation vous sera demandée lors du premier lancement)  


Obtenir la dernière mise à jour
----------------------------------
 Dans la feuille de calcul, aller dans `Outils > Editeur de scripts`, puis `Ressources > Bibliothèques`, choisissez la version la plus récente, puis **cliquez sur Enregistrer**.  
 
![image](https://cloud.githubusercontent.com/assets/1072425/15991503/01a4fe2e-30b5-11e6-82e4-1da6155d48ae.png)


Paramètres utilisateurs
----------------------
Pour indiquer vos propres paramètres, utiliser par la variable `userParams` (dans la feuille de calcul : `Outils > Editeur de scripts`)
exemple :
```
var userParams = {
  showMap: true,
  groupedResults: false
}
```
vous pouvez retrouver les paramètres par défaut par ici : https://github.com/maximelebreton/alertes-leboncoin/blob/master/Code.gs#L9

Un problème ?
--------------
**Avant de vous inquiéter :**  
1. vérifiez que votre **adresse email est bien renseignée** et qu'elle ne contient pas de caractères spéciaux (oui, même le +...)  
2. vérifiez que votre **[version est bien à jour](#obtenir-la-dernière-mise-à-jour)** (et n'oubliez pas de cliquer sur enregistrer lors du changement)  
3. si ça ne fonctionne toujours pas, et que vous ne savez pas pourquoi, tentez une **[réinstallation complète](#installation-en-4-étapes)**  
4. si le problème n'est pas déjà signalé, je vous invite à **[créer une issue](https://github.com/maximelebreton/alertes-leboncoin/issues)**  


Pourquoi ce fork ?
-----------------

**TL DR;**
* refonte totale du code
* intégration de [cheerio](https://github.com/3846masa/cheerio-gasify) (équivalent de jquery côté serveur)
* **mise à jour semi-automatique du code** (`Outils > Editeur de scripts`, puis `Ressources > Bibliothèques` pour choisir la version)
* ajout de paramètres utilisateur
* ajout d'une mini carte pour localiser rapidement l'annonce (`showMap`)
* possibilité de choisir l'envoi des résultats en mails individuels ou en mail groupé (`groupedResults`)

#### > [Vision et évolutions futures de la version 4.x ?](https://github.com/maximelebreton/alertes-leboncoin/issues/2)



Changelog
--------
* **4.1.5** : modification du titre des emails envoyés
* **4.1.4** : ajout d'un footer
* **4.1.3** : Correction d'un bug lié aux paramètres utilisateurs qui n'étaient pas correctement étendus (extend VS deepExtend)
* **4.1.2** : Corrections de bugs, amélioration considérable des performances, données normalisées, et ajout de la possibilité de recevoir des mails individuels
* **4.0** : version initiale du projet (bêta)


_____________________________



v1.x par http://justdocsit.blogspot.fr  
v4.x par [mlb](http://www.maximelebreton.com)  

**Clé projet de la bilbiothèque :** `M9iNq7X9ZWxS_D7pHmMGBb6YoFnfw0_Hk`