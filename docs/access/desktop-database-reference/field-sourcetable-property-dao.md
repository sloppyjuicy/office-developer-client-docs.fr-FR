---
title: Propriété Field.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 9564ea1c-eafd-0b72-fd68-d88fcc3ea189
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197694(v=office.15)
ms:contentKeyID: 48546429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052900
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a557a4941f5b4aa511489c5d057871df5fa72c08
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726063"
---
# <a name="fieldsourcetable-property-dao"></a>Propriété Field.SourceTable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field**. Données de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . SourceTable

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Pour un objet **Field**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ajouté à</p></th>
<th><p>Utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
</tbody>
</table>


Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.


> [!NOTE]
> [!REMARQUE] La propriété **SourceTable** ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet **Field** de la collection **Fields** d'un objet **Recordset** de type table.


