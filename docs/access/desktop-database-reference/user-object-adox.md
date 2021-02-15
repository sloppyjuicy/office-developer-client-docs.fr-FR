---
title: User Object (ADOX - Référence de base de données de bureau Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3299a6c0742e7fcbbd26532f3522fdc96b7956b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313159"
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

