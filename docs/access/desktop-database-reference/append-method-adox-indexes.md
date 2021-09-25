---
title: Append, méthode (Index ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ae56acce889c6931c30603c02869953b2141e210
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559009"
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

