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
ms.translationtype: MT
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

Si vous cliquez sur le bouton **Rechercher** , la\_procédure VBScript Find OnClick Sub, qui génère et envoie la requête SQL, est activée. La grille de données est alors remplie

## <a name="building-the-sql-query"></a>Génération de la requête SQL

La première partie de la procédure\_Find OnClick Sub crée la requête SQL, une expression à la fois, en ajoutant des chaînes de texte à une instruction SQL SELECT globale. Il commence par définir la variable sur une instruction SQL SELECT qui demande toutes les lignes de données de la table de source de données. La procédure Sub analyse ensuite chacune des quatre zones de texte de la page.

Étant donné que le programme utilise le mot dans la création des instructions SQL, les requêtes sont des recherches de sous-chaînes plutôt que des correspondances exactes.

Par exemple, si la zone **nom** contient l'entrée «Berge» et que la zone **titre** contient l'entrée «Program Manager», l'instruction SQL (value of) lirait:

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

Si la requête aboutit, toutes les personnes, dont le nom de famille contient le texte « Berge » (par exemple Berge ou Berger) et dont la fonction contient les termes « Program Manager » (par exemple Program Manager, Advanced Technologies)  sont affichées dans la grille de données HTML.

## <a name="preparing-and-sending-the-query"></a>Préparation et envoi de la requête

La dernière partie de la procédure\_Find OnClick Sub est composée de deux instructions. La première instruction affecte la propriété SQL de l'objet RDS. DataControl est égal à la requête SQL générée dynamiquement. La deuxième instruction provoque l' **objet RDS. DataControl** () pour interroger la base de données, puis afficher les nouveaux résultats de la requête dans la grille.

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a>Mettre à jour le profil

Si vous cliquez sur le bouton **mettre à jour** le\_profil, la procédure de mise à jour OnClick de VBScript, qui exécute l'objet RDS, est activée. DataControl () de l'objet () SubmitChanges et Refresh.

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

Lorsque DC1. SubmitChanges s'exécute, le service de données à distance regroupe toutes les informations de mise à jour et les envoie au serveur via HTTP. La mise à jour est tout-ou-rien; Si une partie de la mise à jour échoue, aucune des modifications n'est apportée et un message d'État est renvoyé. s'exécute, le service de données à distance transmet toutes les informations de mise à jour et les envoie au serveur via HTTP. La mise à jour est tout-ou-rien; Si une partie de la mise à jour échoue, aucune des modifications n'est apportée et un message d'État est renvoyé. DC1. L'actualisation n'est pas nécessaire après **SubmitChanges** avec le service de données à distance, mais elle garantit des données actualisées.

## <a name="cancel-changes-button"></a>Bouton Annuler les modifications

Le fait de cliquer sur **annuler les modifications** active la sous-procédure VBScript Cancel\_OnClick OnClick, qui exécute l'objet RDS. DataControl (méthode CancelUpdate).

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

Quand il s'exécute, il rejette toutes les modifications qu'un utilisateur a apportées à un enregistrement d'employé dans la grille de données depuis la dernière requête ou mise à jour. Elle restaure les valeurs d'origine.

