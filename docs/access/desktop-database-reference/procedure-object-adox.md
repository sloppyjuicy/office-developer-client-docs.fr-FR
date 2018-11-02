---
title: Procedure, objet (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72f0475aeca38b5c6ba6cd2954ff894f00fb6f7f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922649"
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

