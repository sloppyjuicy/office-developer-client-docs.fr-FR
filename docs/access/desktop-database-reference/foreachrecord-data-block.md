---
title: PourChaqueEnregistrement, bloc de données
TOCTitle: ForEachRecord Data Block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dffb433d8a7023b725ebcb5c1e5f651d86f9dbd7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886549"
---
# <a name="foreachrecord-data-block"></a>PourChaqueEnregistrement, bloc de données


**S’applique à**: Access 2013, Office 2013

Un bloc de données **PourChaqueEnregistrement** répète un ensemble d’instructions pour chaque enregistrement dans un domaine.


> [!NOTE]
> <P>[!REMARQUE] Le bloc de données <STRONG>PourChaqueEnregistrement</STRONG> est disponible uniquement dans les macros de données.</P>



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
<td><p>Une chaîne qui identifie le domaine d’enregistrements de fonctionner sur. L’argument <em>dans</em> peut contenir le nom de la table, une requête sélection ou une instruction SQL.</p>

> [!NOTE]
> <P>Le domaine spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.</P>


<p></p></td>
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

