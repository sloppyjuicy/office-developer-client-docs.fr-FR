---
title: Field2.CollatingOrder, propriété (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fa8eac4677018ef1f017996af9d5fc074cb74b9b
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632881"
---
# <a name="field2collatingorder-property-dao"></a>Field2.CollatingOrder, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur **Long** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* CollatingOrder

*expression* une variable qui représente une **champ2** objet.

## <a name="remarks"></a>Remarques

La valeur de retour est une valeur de type **Long** ou une constante pouvant avoir l'une des valeurs suivantes.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Ordre de tri</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbSortGeneral</strong></p></td>
<td><p>Général (Anglais, Français, Allemand, Portugais, Italien et Espagnol moderne)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortArabic</strong></p></td>
<td><p>Arabe</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortChineseSimplified</strong></p></td>
<td><p>Chinois simplifié</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortChineseTraditional</strong></p></td>
<td><p>Chinois traditionnel</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortCyrillic</strong></p></td>
<td><p>Russe</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortCzech</strong></p></td>
<td><p>Tchèque</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortDutch</strong></p></td>
<td><p>Néerlandais</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortGreek</strong></p></td>
<td><p>Grec</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortHebrew</strong></p></td>
<td><p>Hébreu</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortHungungung</strong></p></td>
<td><p>Hongrois</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortIcelandic</strong></p></td>
<td><p>Islandais</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortJapanese</strong></p></td>
<td><p>Japanese</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortKorean</strong></p></td>
<td><p>Korean</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortNeutral</strong></p></td>
<td><p>Neutre</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortNorwDan</strong></p></td>
<td><p>Norvégien ou Danois</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXIntl</strong></p></td>
<td><p>International Paradox</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPDXNor</strong></p></td>
<td><p>Norvégien ou Danois Paradox</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXSwe</strong></p></td>
<td><p>Suédois ou Finnois Paradox</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPolish</strong></p></td>
<td><p>Polonais</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSlovenian</strong></p></td>
<td><p>Slovène</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortSpanish</strong></p></td>
<td><p>Espagnol</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSwedFin</strong></p></td>
<td><p>Suédois ou Finnois</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortThai</strong></p></td>
<td><p>Thaï</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortTurkish</strong></p></td>
<td><p>Turc</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortUndefined</strong></p></td>
<td><p>Non défini ou inconnu</p></td>
</tr>
</tbody>
</table>


La disponibilité de la propriété **CollatingOrder** dépend de l'objet contenant la collection **Fields**, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la collection Fields appartient à un</p></th>
<th><p>Alors CollatingOrder est</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>objet <strong>Index</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>TableDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
</tbody>
</table>


Le **paramètre de la propriété CollatingOrder** correspond à l’argument de paramètres régionaux de la méthode **CreateDatabase** lors de la création de la base de données ou à la méthode **CompactDatabase** lors du dernier compactage de la base de données.

Les paramètres de propriété **CollatingOrder** et **Attributes** d'un objet **Field2** d'une collection **Fields** d'un objet **Index** déterminent ensemble la séquence et la direction de l'ordre de tri dans un index. Toutefois, vous ne pouvez définir aucun ordre de tri pour un index individuel, vous pouvez uniquement le faire pour une table entière.

