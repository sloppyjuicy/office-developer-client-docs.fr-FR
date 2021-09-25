---
title: User Object (ADOX - Référence de base de données de bureau Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8bd62da5b813985c725703cca80a75aabbac73fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593354"
---
# <a name="user-object-adox"></a>Objet User (ADOX)


**S’applique à** : Access 2013, Office 2013

Représente un compte d'utilisateur qui dispose d'autorisations d'accès à une base de données sécurisée.

## <a name="remarks"></a>Remarques

La collection [Users](users-collection-adox.md) d’un [catalogue](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d’un [groupe](group-object-adox.md) représente les utilisateurs du groupe spécifique uniquement.

Avec les propriétés, collections et méthodes d'un objet **User**, vous pouvez :

  - Identifier l’utilisateur à l’aide de la propriété [Name](name-property-adox.md).

  - Modifier le mot de passe d’un utilisateur à l’aide de la méthode [ChangePassword](changepassword-method-adox.md).

  - Déterminer si un utilisateur dispose des autorisations de lecture, écriture ou suppression à l’aide des méthodes [GetPermissions](getpermissions-method-adox.md) et [SetPermissions](setpermissions-method-adox.md).

  - Accéder aux groupes auxquels un utilisateur appartient à l’aide de la collection [Groups](groups-collection-adox.md).

  - Accéder aux propriétés spécifiques au fournisseur à l’aide de la collection [Properties](properties-collection-ado.md).

