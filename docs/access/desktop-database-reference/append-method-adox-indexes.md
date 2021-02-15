---
title: Append, méthode (Index ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0b541512de9748e94d033bb56f27dd0941c7f5a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297094"
---
# <a name="append-method-adox-indexes"></a>Append, méthode (Index ADOX)


**S’applique à** : Access 2013, Office 2013



Ajoute un nouvel objet [Index](index-object-adox.md) à la collection [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Index .* Append *Index* \[ ,*Columns*\]

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Index* |Objet **Index** à ajouter ou nom de l'index à créer et à ajouter.|
|*Columns* |Facultatif. Valeur de type **Variant** qui spécifie le ou les noms des colonne à indexer. Le paramètre *Column* correspond à la ou aux valeurs de la propriété [Name](name-property-adox.md) d’un ou plusieurs objets [Column](column-object-adox.md).|

## <a name="remarks"></a>Remarques

Le paramètre *Columns* peut prendre soit le nom d'une colonne, soit une matrice de noms de colonne.

Une erreur se produit si le fournisseur ne prend pas en charge la création d'index.

