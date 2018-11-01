---
title: ModifierEnregistrement, bloc de données
TOCTitle: EditRecord Data Block
ms:assetid: fe9f55eb-d7ed-1914-65a9-fa2fcb332b98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837277(v=office.15)
ms:contentKeyID: 48548940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9c4d5a5a1565aeda41e5a52127e9f82b5304e686
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876882"
---
# <a name="editrecord-data-block"></a>ModifierEnregistrement, bloc de données

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser le bloc de données **ModifierEnregistrement** pour modifier les valeurs contenues dans un enregistrement existant.

> [!NOTE]
> [!REMARQUE] Le bloc de données **ModifierEnregistrement** est disponible uniquement dans les macros de données.


## <a name="setting"></a>Paramètre

Le bloc de données **ModifierEnregistrement** utilise les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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

## <a name="remarks"></a>Notes

Après l'instruction **ModifierEnregistrement**, vous pouvez insérer un bloc de commandes qui sera exécuté avant la validation des modifications apportées à l'enregistrement. Les actions suivantes sont disponibles dans un bloc de données **ModifierEnregistrement**.

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="cancelrecordchange-macro-action.md">Action de Macro AnnulerModificationEnregistrement</a></p></td>
</tr>
<tr class="even">
<td><p><a href="comment-macro-statement.md">Instruction de Macro commentaire</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="group-macro-statement.md">Group, instruction de Macro</a></p></td>
</tr>
<tr class="even">
<td><p><a href="if-then-else-macro-block.md">If... Procédez comme suit... Else, instruction de Macro</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="setfield-macro-action.md">Action de Macro SetField</a></p></td>
</tr>
<tr class="even">
<td><p><a href="setlocalvar-macro-action.md">Action de Macro DéfinirVarLocale</a></p></td>
</tr>
</tbody>
</table>

Utilisez l'action **DéfinirChamp** pour spécifier les nouvelles valeurs d'un champ dans l'enregistrement modifié.

Vous pouvez utiliser une instruction **If... Then... Else** pour effectuer des opérations basées sur une condition.

Pour annuler la modification d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **ModifierEnregistrement**.

Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement :

`[LastCreateRecordIdentity].[AssignedTo]`

Le bloc de données CréerEnregistrement peut être utilisé uniquement dans les événements de macros de données **[Après insertion](after-insert-macro-event.md)**, **[Après MAJ](after-update-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.

