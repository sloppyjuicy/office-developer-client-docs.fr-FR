---
title: Objet Group (ADOX)
TOCTitle: Group object (ADOX)
ms:assetid: 91cf1b87-c928-1d89-2731-138f6299cc60
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249642(v=office.15)
ms:contentKeyID: 48546359
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3d131d89dbcc67f244010fc0cee86bad30f78c2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606694"
---
# <a name="group-object-adox"></a>Objet Group (ADOX)


**S’applique à** : Access 2013, Office 2013

Représente un compte de groupe disposant des autorisations d'accès à une base de données sécurisée.

## <a name="remarks"></a>Remarques

La collection [Groups](groups-collection-adox.md) d'un [catalogue](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un [utilisateur](user-object-adox.md) représente le groupe auquel l'utilisateur appartient uniquement.

Avec les propriétés, collections et méthodes d'un objet **Group**, vous pouvez :

  - Identifier le groupe à l'aide de la propriété [Name](name-property-adox.md).

  - Déterminer si un groupe dispose des autorisations de lecture, écriture ou suppression à l'aide des méthodes [GetPermissions](getpermissions-method-adox.md) et [SetPermissions](setpermissions-method-adox.md).

  - Accéder aux comptes d'utilisateurs appartenant au groupe à l'aide de la collection [Users](users-collection-adox.md).

  - Accéder aux propriétés spécifiques au fournisseur à l’aide de la collection [Properties](properties-collection-ado.md).

