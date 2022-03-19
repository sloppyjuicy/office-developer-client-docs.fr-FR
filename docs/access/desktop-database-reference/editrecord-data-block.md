---
title: Bloc de données EditRecord
TOCTitle: EditRecord data block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7d22c36117b18bf52c3f6a32a17da43a92b200c3
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628333"
---
# <a name="editrecord-data-block"></a>Bloc de données EditRecord

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser le bloc de données **ModifierEnregistrement** pour modifier les valeurs contenues dans un enregistrement existant.

> [!NOTE]
> Le bloc de données **ModifierEnregistrement** est disponible uniquement dans les macros de données.


## <a name="setting"></a>Paramètres

Le bloc de données **ModifierEnregistrement** utilise les arguments suivants.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Alias</strong></p></td>
<td><p>Chaîne qui identifie l’enregistrement à modifier. Si l’argument <em>Alias</em> n’est pas spécifié, l’enregistrement actif est modifié.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Après l'instruction **ModifierEnregistrement**, vous pouvez insérer un bloc de commandes qui sera exécuté avant la validation des modifications apportées à l'enregistrement. Les actions suivantes sont disponibles dans un bloc de données **ModifierEnregistrement**.

<table>
<colgroup>
<col />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Comment, instruction de macro</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Group, instruction de macro</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">Si... Ensuite... Instruction de macro Else</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">SetField, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar, action de macro</a></p></td>
</tr>
</tbody>
</table>

Utilisez l'action **DéfinirChamp** pour spécifier les nouvelles valeurs d'un champ dans l'enregistrement modifié.

Vous pouvez utiliser une instruction **If... Then... Else** pour effectuer des opérations basées sur une condition.

Pour annuler la modification d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **ModifierEnregistrement**.

Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement créé :

`[LastCreateRecordIdentity].[AssignedTo]`

Le bloc de données CréerEnregistrement peut être utilisé uniquement dans les événements de macros de données **[Après insertion](after-insert-macro-event.md)**, **[Après MAJ](after-update-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.

