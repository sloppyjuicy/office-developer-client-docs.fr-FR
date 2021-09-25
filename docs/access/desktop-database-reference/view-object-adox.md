---
title: View Object (ADOX - Référence de base de données de bureau Access)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 25135ed00041aa9b5e5e5a7089d721d7b6e9da1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568340"
---
# <a name="view-object-adox"></a>View, objet (ADOX)


**S’applique à** : Access 2013, Office 2013

Représente un jeu d'enregistrements filtré ou une table virtuelle. Utilisé avec l'objet ADO [Command](command-object-ado.md), l'objet **View** permet d'ajouter, de supprimer ou de modifier des vues.

## <a name="remarks"></a>Remarques

Une vue est une table virtuelle créée à partir d'autres tables ou vues de base de données. Les objets **View** vous permettent de créer une vue sans avoir à connaître ou utiliser la syntaxe « CREATE VIEW » du fournisseur.

Avec les propriétés d'un objet **View**, vous pouvez :

  - Identifier la vue à l'aide de la propriété [Name](name-property-adox.md).

  - Spécifier l'objet ADO **Command** à utiliser pour ajouter, supprimer ou modifier les vues à l'aide de la propriété [Command](command-property-adox.md).

  - Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).

