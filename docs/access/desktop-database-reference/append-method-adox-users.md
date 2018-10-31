---
title: Append, méthode (Utilisateurs ADOX)
TOCTitle: Append Method (ADOX Users)
ms:assetid: b7a1128b-c6e7-2071-c914-913b6bd245ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249884(v=office.15)
ms:contentKeyID: 48547302
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dc8f7a2d217a25a8404765aa05bae19fdccad2c3
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863863"
---
# <a name="append-method-adox-users"></a>Append, méthode (Utilisateurs ADOX)


**S’applique à**: Access 2013 | Office 2013


Ajoute un nouvel objet [User](user-object-adox.md) à la collection [Users](users-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Les utilisateurs*. Ajouter*l’utilisateur*\[,*le mot de passe*\]

## <a name="parameters"></a>Paramètres

  - *User*

  - Valeur de type **Variant** qui contient l'objet **User** à ajouter ou le nom de l'utilisateur à créer et à ajouter.

  - *Password*

  - Facultatif. Valeur de type **String** qui contient le mot de passe de l'utilisateur. Le paramètre *Password* correspond à la valeur spécifiée par la méthode [ChangePassword](changepassword-method-adox.md) d’un objet **utilisateur** .

## <a name="remarks"></a>Remarques

La collection **Users** d'un objet [Catalog](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un objet [Group](group-object-adox.md) représente uniquement les utilisateurs qui appartiennent à ce groupe.

Une erreur se produit si le fournisseur ne prend pas en charge la création d'utilisateurs.


> [!NOTE]
> [!REMARQUE] Avant d'ajouter un objet **User** à la collection **Users** d'un objet **Group**, un objet **User** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Users** de l'objet **Catalog**.


