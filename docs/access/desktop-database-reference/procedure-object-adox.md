---
title: Procedure, objet (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afc4eae76395e7a15573ad5343955b0ab46df3db
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883350"
---
# <a name="procedure-object-adox"></a>Procedure, objet (ADOX)


**S’applique à**: Access 2013, Office 2013

Représente une procédure stockée. Utilisé avec l'objet ADO [Command](command-object-ado.md), l'objet **Procedure** permet d'ajouter, de supprimer ou de modifier des procédures stockées.

## <a name="remarks"></a>Remarques

L'objet **Procedure** vous permet de créer une procédure stockée sans avoir à connaître ou à utiliser la syntaxe « CREATE PROCEDURE » du fournisseur.

Avec les propriétés d'un objet **Procedure**, vous pouvez :

  - Identifier la procédure à l'aide de la propriété [Name](name-property-adox.md).

  - Spécifier l'objet ADO **Command** à utiliser pour créer ou exécuter la procédure à l'aide de la propriété [Command](command-property-adox.md).

  - Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).

