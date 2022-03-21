---
title: Field.SourceField, propriété (DAO)
TOCTitle: SourceField Property
ms:assetid: e5750d6c-4078-7bbb-9356-f9207c4e8028
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835953(v=office.15)
ms:contentKeyID: 48548360
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 14887435eac173ac5bd97b43c52e43f046301009
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632888"
---
# <a name="fieldsourcefield-property-dao"></a>Field.SourceField, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur spécifiant le nom du champ qui représente la source d'origine des données d'un objet **Field**. Type **String** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* SourceField

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Pour un objet **Field**, l'utilisation des propriétés **SourceField** et **SourceTable** dépend de l'objet contenant la collection **Fields** à laquelle l'objet **Field** est ajouté, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col />
<col />
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


Ces propriétés indiquent les noms des tables et des champs d'origine associés à un objet **Field**. Vous pouvez, par exemple, utiliser ces propriétés pour déterminer la source d'origine des données dans un champ de requête dont le nom n'a aucun rapport avec le nom du champ dans la table sous-jacente.

