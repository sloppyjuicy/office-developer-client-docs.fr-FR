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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707555"
---
# <a name="append-method-adox-indexes"></a>Append, méthode (Index ADOX)


**S’applique à**: Access 2013, Office 2013



Ajoute un nouvel objet [Index](index-object-adox.md) à la collection [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Index*. Ajouter des*Index* \[,*colonnes*\]

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Index* |Objet **Index** à ajouter ou nom de l'index à créer et à ajouter.|
|*Columns* |Facultatif. Valeur de type **Variant** qui spécifie le ou les noms des colonne à indexer. Le paramètre *Columns* correspond à l’ou les valeurs de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) ou des objets.|

## <a name="remarks"></a>Remarques

Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.

Une erreur se produit si le fournisseur ne prend pas en charge la création d'index.

