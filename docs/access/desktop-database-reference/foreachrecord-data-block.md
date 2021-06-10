---
title: Bloc de données ForEachRecord
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292327"
---
# <a name="foreachrecord-data-block"></a>Bloc de données ForEachRecord

**S’applique à** : Access 2013, Office 2013

Un **bloc de données ForEachRecord** répète un ensemble d’instructions pour chaque enregistrement d’un domaine.

> [!NOTE]
> Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètre

L’action **PourChaqueEnregistrement** utilise les arguments suivants.

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
<td><p>Chaîne qui identifie le domaine d’enregistrements sur lequel opérer. <em>L’argument In</em> peut contenir le nom de la table, une requête Select ou une SQL instruction.</p><p><strong>REMARQUE</strong>: le domaine spécifié ne peut pas inclure les données stockées dans une table liée ou une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condition Where</strong></p></td>
<td><p>Non</p></td>
<td><p>Expression de chaîne utilisée pour limiter la plage de données sur laquelle le bloc de données <strong>ForEachRecord</strong> est effectué. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. Si des critères sont omis, le bloc de données <strong>ForEachRecord</strong> fonctionne sur l’intégralité du domaine spécifié par <em>l’argument In.</em> Tout champ inclus dans les critères doit également être un champ dans <em>In</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui fournit un autre nom pour le domaine spécifié par l’argument <em>In.</em> Souvent utilisé pour raccourcir le nom de la table pour les références suivantes afin d’éviter les références ambiguës possibles. Si <em>l’alias</em> n’est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.

