---
title: Propriété Field2.SourceTable (DAO)
TOCTitle: SourceTable Property
ms:assetid: 24d2fdda-d924-d95e-8458-063dd1d36d5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191839(v=office.15)
ms:contentKeyID: 48543768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fbde7aa9785e4e875f96569884e7f6e45743f2bb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925582"
---
# <a name="field2sourcetable-property-dao"></a>Propriété Field2.SourceTable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet **Field2**. Données de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . SourceTable

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Pour un objet **Field2**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.

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
<td><p><strong>Objet QueryDef</strong></p></td>
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


Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field2**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.


> [!NOTE]
> <P>[!REMARQUE] La propriété <STRONG>SourceTable</STRONG> ne renvoie aucun nom de table significatif lorsqu'elle est utilisée sur un objet <STRONG>Field2</STRONG> de la collection <STRONG>Fields</STRONG> d'un objet <STRONG>Recordset</STRONG> de type table.</P>


