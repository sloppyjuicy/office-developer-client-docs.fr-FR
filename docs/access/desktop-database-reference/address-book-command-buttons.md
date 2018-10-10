---
title: Boutons de commande du Carnet d'adresses
TOCTitle: Address Book Command Buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15a79db455032ddf2eb9fa0d9555d8f7a4959313
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472285"
---
# <a name="address-book-command-buttons"></a>Boutons de commande du Carnet d'adresses


**S’applique à**: Access 2013 | Office 2013


L'application Carnet d'adresses comprend les boutons de commande suivants :

  - Rechercher pour envoyer une requête à la base de données ;

  - **Effacer** pour effacer les zones de texte avant de lancer une nouvelle recherche ;

  - Mettre à jour le profil pour sauvegarder les modifications apportées à l'enregistrement d'un employé.

  - Annuler les modifications afin d'ignorer les modifications.

## <a name="find-button"></a>Bouton Rechercher

En cliquant sur le bouton **Rechercher** Active la rechercher VBScript\_procédure OnClick Sub, qui crée et envoie la requête SQL. La grille de données est alors remplie

## <a name="building-the-sql-query"></a>Génération de la requête SQL

La première partie de la recherche\_procédure OnClick Sub génère la requête SQL, une phrase à la fois, en ajoutant des chaînes de texte à une instruction SQL SELECT globale. Il commence par la définition de la variable à une instruction SQL SELECT qui demande toutes les lignes de données à partir de la table de source de données. La procédure Sub analyse ensuite chacune des quatre zones de texte de la page.

Étant donné que le programme utilise le mot de la création des instructions SQL, les requêtes sont des recherches de sous-chaînes plutôt que des correspondances exactes.

Par exemple, si la zone **Nom de famille** contenue l’entrée « Berge » et que la zone de **titre** contenue l’entrée « Program Manager », l’instruction SQL (valeur) se présente alors :

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Si la requête aboutit, toutes les personnes, dont le nom de famille contient le texte « Berge » (par exemple Berge ou Berger) et dont la fonction contient les termes « Program Manager » (par exemple Program Manager, Advanced Technologies) sont affichées dans la grille de données HTML.

## <a name="preparing-and-sending-the-query"></a>Préparation et envoi de la requête

La dernière partie de la recherche\_procédure OnClick Sub se compose de deux instructions. La première instruction affecte à la propriété SQL de l’objet RDS. Objet DataControl est égale à la requête. La deuxième instruction provoque la **RDS. DataControl** () pour interroger la base de données d’objet, puis afficher les résultats de la requête dans la grille.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Mettre à jour le profil

Le bouton **Mise à jour le profil** permet d’activer la mise à jour VBScript\_procédure OnClick Sub, l’objet RDS. Méthodes SubmitChanges et Refresh de () de l’objet DataControl.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Lorsque DC1. SubmitChanges s’exécute, le Service de données distant regroupe toutes les informations de mise à jour et l’envoie au serveur via HTTP. La mise à jour est tout ou rien ; Si une partie de la mise à jour échoue, aucune modification est effectuée et un message d’état est retourné. s’exécute, le Service de données distant regroupe toutes les informations de mise à jour et l’envoie au serveur via HTTP. La mise à jour est tout ou rien ; Si une partie de la mise à jour échoue, aucune modification est effectuée et un message d’état est retourné. DC1. Actualisation n’est pas nécessaire après **SubmitChanges** via le Service RDS mais elle garantit des données actualisées.

## <a name="cancel-changes-button"></a>Bouton Annuler les modifications

**Annuler les modifications** permet d’activer l’annulation VBScript\_procédure OnClick Sub, l’objet RDS. DataControl, objet (méthode CancelUpdate.

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Lorsque s’exécute, il ignore les modifications qu’un utilisateur a apportées à un enregistrement d’employé dans la grille de données depuis la dernière requête ou mise à jour. Elle restaure les valeurs d'origine.

