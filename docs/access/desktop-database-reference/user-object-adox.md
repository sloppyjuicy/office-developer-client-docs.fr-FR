---
title: User, objet (ADOX - référence du bureau de la base de données Access)
TOCTitle: User object (ADOX)
ms:assetid: e88b9a8a-e70f-c7ca-cb8c-bd274ff24948
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250178(v=office.15)
ms:contentKeyID: 48548426
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 845697f54ea5e37e051836896b84d8a3ff061237
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919878"
---
# <a name="user-object-adox"></a>User, objet (ADOX)


**S’applique à**: Access 2013, Office 2013

Représente un compte d'utilisateur qui dispose d'autorisations d'accès à une base de données sécurisée.

## <a name="remarks"></a>Remarques

La collection [Users](users-collection-adox.md) d'un [catalogue](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un [groupe](group-object-adox.md) représente les utilisateurs du groupe spécifique uniquement.

Avec les propriétés, collections et méthodes d'un objet **User**, vous pouvez :

  - Identifier l'utilisateur à l'aide de la propriété [Name](name-property-adox.md).

  - Modifier le mot de passe d'un utilisateur à l'aide de la méthode [ChangePassword](changepassword-method-adox.md).

  - Déterminer si un utilisateur dispose des autorisations de lecture, écriture ou suppression à l'aide des méthodes [GetPermissions](getpermissions-method-adox.md) et [SetPermissions](setpermissions-method-adox.md).

  - Accéder aux groupes auxquels un utilisateur appartient à l'aide de la collection [Groups](groups-collection-adox.md).

  - Accéder aux propriétés spécifiques au fournisseur à l'aide de la collection [Properties](properties-collection-ado.md).

