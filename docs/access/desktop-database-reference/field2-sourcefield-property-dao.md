---
title: Field2.SourceField, propriété (DAO)
TOCTitle: SourceField Property
ms:assetid: f89146c1-d4a4-1129-636a-c22cf7921a4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836948(v=office.15)
ms:contentKeyID: 48548784
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c86f38479915a962f1e1a34030e968fbf019b20b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602660"
---
# <a name="field2sourcefield-property-dao"></a>Field2.SourceField, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur indiquant le nom du champ duquel provient les données d'un objet **Field2**. Données de type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* SourceField

*expression* une variable qui représente une **champ2** objet.

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
<td><p>Non reconnu</p></td>
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
<td><p>Non reconnu</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
</tbody>
</table>


Ces propriétés indiquent le champ d'origine et les noms de table associés à un objet **Field2**. Par exemple, vous pouvez utiliser ces propriétés pour déterminer la source d'origine des données d'un champ de requête dont le nom n'est pas associé au nom du champ de la table sous-jacente.

