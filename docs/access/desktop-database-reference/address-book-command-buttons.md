---
title: Boutons de commande de Carnet d’adresses
TOCTitle: Address Book command buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 09f2513a3c541c76352e773f7f2a8f0c24f78850
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282477"
---
# <a name="address-book-command-buttons"></a>Boutons de commande de Carnet d’adresses


**S’applique à** : Access 2013, Office 2013


L'application Carnet d'adresses comprend les boutons de commande suivants :

- **Rechercher** pour envoyer une requête à la base de données ;

- **Effacer** pour effacer les zones de texte avant de lancer une nouvelle recherche ;

- **Mettre à jour le profil** pour sauvegarder les modifications apportées à l'enregistrement d'un employé.

- **Annuler les modifications** afin d'ignorer les modifications.

## <a name="find-button"></a>Bouton Rechercher

Le bouton **Rechercher** active la procédure Sub « Find\_OnClick » VBScript chargée de créer et d'envoyer la requête SQL. La grille de données est alors remplie

## <a name="building-the-sql-query"></a>Génération de la requête SQL

La première partie de la procédure Sub « Find\_OnClick » génère la requête SQL, expression par expression, en ajoutant des chaînes de texte à une instruction SQL SELECT globale. Elle commence par définir la variable à une instruction SQL SELECT chargée de demander toutes les lignes de données de la table de sources de données. La procédure Sub analyse ensuite chacune des quatre zones de texte de la page.

Étant donné que le programme utilise le mot lors de la création des instructions SQL, les requêtes sont des recherches de sous-chaînes plutôt que des correspondances exactes.

Par exemple, si la zone **Last Name** (Nom de famille) contient l'entrée « Berge » et que la zone **Title** (Fonction) contient l'entrée « Program Manager » (Responsable de programme), l'instruction SQL (c'est-à-dire la valeur de) lit ::

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Si la requête aboutit, toutes les personnes, dont le nom de famille contient le texte « Berge » (par exemple Berge ou Berger) et dont la fonction contient les termes « Program Manager » (par exemple Program Manager, Advanced Technologies)  sont affichées dans la grille de données HTML.

## <a name="preparing-and-sending-the-query"></a>Préparation et envoi de la requête

La dernière partie de la procédure Sub Find\_OnClick se compose de deux instructions. La première instruction attribue la propriété SQL de l’objet RDS.DataControl égal à la requête SQL intégrée de façon dynamique. La deuxième déclaration provoque l'objet **RDS.DataControl** () pour interroger la base de données, puis afficher les nouveaux résultats de la requête dans la grille.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Bouton Mettre à jour le profil

Le bouton **Mettre à jour le profil** permet d’activer la procédure Sub VBScript Update\_OnClick chargée d’exécuter les méthodes SubmitChanges et Refresh de l’objet RDS.DataControl ().

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Lorsque le DC1.SubmitChanges s'exécute, le service de données distants met en package toutes les informations de mise à jour et les envoie au serveur via HTTP. La mise à jour est de type « tout-ou-rien » : si une partie de la mise à jour ne se déroule pas correctement, aucune modification n'est appliquée et un message d'état est retourné. s'exécute, le service de données distants met en package toutes les informations de mise à jour et les envoie au serveur via HTTP. La mise à jour est de type « tout-ou-rien » : si une partie de la mise à jour ne se déroule pas correctement, aucune modification n'est appliquée et un message d'état est retourné. DC1.Refresh n'est pas nécessaire après l'utilisation de **SubmitChanges** via le service RDS mais elle garantit des données actualisées.

## <a name="cancel-changes-button"></a>Bouton Annuler les modifications

Le bouton **Annuler les modifications** permet d’activer la procédure Sub VBScript Update\_OnClick chargée d’exécuter la méthode CancelUpdate de l’objet RDS.DataControl.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Lors de son exécution, l'instruction ignore toutes les modifications qu'un utilisateur a apportées à l'enregistrement d'un employé dans la grille de données depuis la dernière requête ou mise à jour. Elle restaure les valeurs d'origine.

