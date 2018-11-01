---
title: Objet View (référence de base de données du bureau Access - ADOX)
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e1c3b2cc99cad4ba3b9ee71f0c44ee67b32d41d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873130"
---
# <a name="view-object-adox"></a>View, objet (ADOX)


**S’applique à**: Access 2013, Office 2013

Représente un jeu d'enregistrements filtré ou une table virtuelle. Utilisé avec l'objet ADO [Command](command-object-ado.md), l'objet **View** permet d'ajouter, de supprimer ou de modifier des vues.

## <a name="remarks"></a>Remarques

Une vue est une table virtuelle créée à partir d'autres tables ou vues de base de données. Les objets **View** vous permettent de créer une vue sans avoir à connaître ou utiliser la syntaxe « CREATE VIEW » du fournisseur.

Avec les propriétés d'un objet **View**, vous pouvez :

  - Identifier la vue à l'aide de la propriété [Name](name-property-adox.md).

  - Spécifier l'objet ADO **Command** à utiliser pour ajouter, supprimer ou modifier les vues à l'aide de la propriété [Command](command-property-adox.md).

  - Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).

