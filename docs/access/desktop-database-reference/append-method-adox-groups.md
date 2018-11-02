---
title: Append, méthode (Groupes ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dfc2da5490cf5c148d39670dedfb2551cedd31f2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923587"
---
# <a name="append-method-adox-groups"></a>Append, méthode (Groupes ADOX)


**S’applique à**: Access 2013, Office 2013



Ajoute un nouvel objet [Group](group-object-adox.md) à la collection [Groups](groups-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Groupes*. Ajouter le*groupe*

## <a name="parameters"></a>Paramètres

  - *Group*

  - Objet **Group** à ajouter ou nom du groupe à créer et à ajouter.

## <a name="remarks"></a>Notes

La collection **Groups** d'un objet [Catalog](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un objet [User](user-object-adox.md) contient uniquement le groupe auquel l'utilisateur appartient.

Une erreur se produit si le fournisseur ne prend pas en charge la création de groupes.


> [!NOTE]
> [!REMARQUE] Avant d'ajouter un objet **Group** à la collection **Groups** d'un objet **User**, un objet **Group** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Groups** de l'objet **Catalog**.


