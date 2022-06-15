---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ec62ba3b1bd8d7e15abb48f67ef1c7a3ae48cc48
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083835"
---
# <a name="append-method-adox-columns"></a>Append, méthode (Colonnes ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Colonnes*. Ajouter *une colonne* \[, *type*\] \[, *DefinedSize*\]

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Column* |Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.|
|*Type* |Facultatif. Valeur de type **long** qui spécifie le type de données de la colonne. Le paramètre *Type* correspond à la propriété [Type](/office/vba/access/concepts/miscellaneous/type-property-columnadox) d’un objet **Column**.|
|*DefinedSize* |Facultatif. Valeur de type **long** qui spécifie la taille de la colonne. Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’
un objet **Column**.|


> [!NOTE]
> Une erreur se produit en cas d’ajout d’un objet **Column** à la collection **Columns** d’un objet [Index](index-object-adox.md) si l’objet **Column** n’existe pas dans un objet [Table](table-object-adox.md) déjà ajouté à la collection [Tables](tables-collection-adox.md).
