---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2827fa16ce33903b7e220797ea51d4098b866e7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559044"
---
# <a name="append-method-adox-columns"></a>Append, méthode (Colonnes ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Colonnes*. Append *Column* \[ ,*Type* \] \[ ,*DefinedSize*\]

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Column* |Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.|
|*Type* |Facultatif. Valeur de type **long** qui spécifie le type de données de la colonne. Le paramètre *Type* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) d’un objet **Column**.|
|*DefinedSize* |Facultatif. Valeur de type **long** qui spécifie la taille de la colonne. Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’
un objet **Column**.|


> [!NOTE]
> Une erreur se produit en cas d’ajout d’un objet **Column** à la collection **Columns** d’un objet [Index](index-object-adox.md) si l’objet **Column** n’existe pas dans un objet [Table](table-object-adox.md) déjà ajouté à la collection [Tables](tables-collection-adox.md).


