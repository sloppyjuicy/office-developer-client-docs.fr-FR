---
title: PourChaqueEnregistrement, bloc de données
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
# <a name="foreachrecord-data-block"></a>PourChaqueEnregistrement, bloc de données

**S’applique à** : Access 2013, Office 2013

Un bloc de données **PourChaqueEnregistrement** répète un ensemble d'instructions pour chaque enregistrement dans un domaine.

> [!NOTE]
> Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Setting

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
<td><p><strong>Dans</strong></p></td>
<td><p>Oui</p></td>
<td><p>Chaîne qui identifie le domaine d’enregistrements sur lequel opérer. L'argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</p><p><strong>Remarque</strong>: le domaine spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condition Where</strong></p></td>
<td><p>Non</p></td>
<td><p>Expression de chaîne servant à limiter la plage de données sur laquelle le bloc de données <strong>PourChaqueEnregistrement</strong> est exécuté. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. En cas d'omission de critère, le bloc de données <strong>PourChaqueEnregistrement</strong> s'applique à l'ensemble du domaine spécifié par l'argument <em>in</em> . Tout champ inclus dans les critères doit également être un champ dans <em>In</em>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui fournit un autre nom pour le domaine spécifié par l'argument <em>dans</em> . Souvent utilisé pour raccourcir le nom de la table pour les références ultérieures afin d'éviter d'éventuelles références ambiguës. Si <em>alias</em> n'est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**.

