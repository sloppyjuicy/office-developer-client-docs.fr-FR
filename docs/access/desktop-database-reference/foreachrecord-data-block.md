---
title: Bloc de données PourChaqueEnregistrement
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706344"
---
# <a name="foreachrecord-data-block"></a>Bloc de données PourChaqueEnregistrement

**S’applique à**: Access 2013, Office 2013

Un bloc de données **PourChaqueEnregistrement** répète un ensemble d’instructions pour chaque enregistrement dans un domaine.

> [!NOTE]
> [!REMARQUE] Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètre

L'action **PourChaqueEnregistrement** utilise les arguments suivants.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatoire</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>In</strong></p></td>
<td><p>Oui</p></td>
<td><p>Une chaîne qui identifie le domaine d’enregistrements de fonctionner sur. L’argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</p><p><strong>Remarque</strong>: le domaine spécifié ne peut pas inclure les données stockées dans une table liée ou d’une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Where Condition</strong></p></td>
<td><p>Non</p></td>
<td><p>Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données <strong>PourChaqueEnregistrement</strong> est effectuée. Par exemple, critères est souvent équivalent à la clause WHERE d’une expression SQL sans le mot où. Si l’argument critères est omis, le bloc de données <strong>PourChaqueEnregistrement</strong> opère sur l’intégralité du domaine spécifié par l’argument <em>dans</em> . Un champ qui est inclus dans les critères doit également être un champ <em>dans</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui fournit un autre nom pour le domaine spécifié par l’argument <em>dans</em> . Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus. Si <em>Alias</em> n’est pas spécifié, le nom de la table ou requête sera utilisé comme alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.

