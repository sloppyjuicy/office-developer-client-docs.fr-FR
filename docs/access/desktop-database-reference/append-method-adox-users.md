---
title: Append, méthode (Utilisateurs ADOX)
TOCTitle: Append method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d05cf352515d8fe4faa868088c9ba9cc8a024145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297066"
---
# <a name="append-method-adox-users"></a>Append, méthode (Utilisateurs ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [User](user-object-adox.md) à la collection [Users](users-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Les utilisateurs*. Ajouter un*utilisateur*\[,*mot de passe*\]

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*User* |Valeur de type **Variant** qui contient l'objet **User** à ajouter ou le nom de l'utilisateur à créer et à ajouter.|
|*Password* |Facultatif. Valeur de type **String** qui contient le mot de passe de l’utilisateur. Le paramètre *Password* correspond à la valeur spécifiée par la méthode [ChangePassword](changepassword-method-adox.md) d’un objet **User**.|

## <a name="remarks"></a>Remarques

La collection **Users** d'un objet [Catalog](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un objet [Group](group-object-adox.md) représente uniquement les utilisateurs qui appartiennent à ce groupe.

Une erreur se produit si le fournisseur ne prend pas en charge la création d'utilisateurs.

> [!NOTE]
> [!REMARQUE] Avant d'ajouter un objet **User** à la collection **Users** d'un objet **Group**, un objet **User** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Users** de l'objet **Catalog**.


