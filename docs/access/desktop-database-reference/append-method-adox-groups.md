---
title: Append, méthode (Groupes ADOX)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0e7731777e3d82e3746c3886bdbddb3e43db66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297101"
---
# <a name="append-method-adox-groups"></a>Append, méthode (Groupes ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [Group](group-object-adox.md) à la collection [Groups](groups-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Groupes*. Ajouter un*groupe*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*Group* |Objet **Group** à ajouter ou nom du groupe à créer et à ajouter.|

## <a name="remarks"></a>Remarques

La collection **Groups** d'un objet [Catalog](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un objet [User](user-object-adox.md) contient uniquement le groupe auquel l'utilisateur appartient.

Une erreur se produit si le fournisseur ne prend pas en charge la création de groupes.

> [!NOTE]
> [!REMARQUE] Avant d'ajouter un objet **Group** à la collection **Groups** d'un objet **User**, un objet **Group** affecté de la même propriété [Name](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Groups** de l'objet **Catalog**.


