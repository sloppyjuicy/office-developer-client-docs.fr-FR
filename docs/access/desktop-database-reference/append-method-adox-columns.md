---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 48bc100b7b56265a570ce963b80f569f1d827150
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297122"
---
# <a name="append-method-adox-columns"></a>Append, méthode (Colonnes ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Colonnes*. Append,*colonne* \[,*type* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*Column* |Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.|
|*Type* |Facultatif. Valeur de type **long** qui spécifie le type de données de la colonne. Le paramètre *Type* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) d’un objet **Column**.|
|*DefinedSize* |Facultatif. Valeur de type **long** qui spécifie la taille de la colonne. Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’
un objet **Column**.|


> [!NOTE]
> Une erreur se produit en cas d’ajout d’un objet **Column** à la collection **Columns** d’un objet [Index](index-object-adox.md) si l’objet **Column** n’existe pas dans un objet [Table](table-object-adox.md) déjà ajouté à la collection [Tables](tables-collection-adox.md).


