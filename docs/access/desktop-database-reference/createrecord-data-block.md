---
title: Bloc de données CreateRecord
TOCTitle: CreateRecord data block
ms:assetid: e18f47f8-2aad-9a14-ad63-ab603a4d5b07
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835671(v=office.15)
ms:contentKeyID: 48548263
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2430e3731f83c59eb039f504609772cdc69b9695
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581594"
---
# <a name="createrecord-data-block"></a>Bloc de données CreateRecord


**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée.

> [!NOTE]
> Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Paramètre

Le bloc de données **CréerEnregistrement** utilise les arguments suivants.

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
<td><p><strong>Créer un enregistrement dans</strong></p></td>
<td><p>Oui</p></td>
<td><p>Nom de la table dans laquelle créer le nouvel enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alias</strong></p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui identifie l’enregistrement. Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L’enregistrement créé par **CréerEnregistrement** devient automatiquement l’enregistrement actif.

Après **l’instruction CreateRecord,** vous pouvez insérer un bloc de commandes qui s’exécute avant que le nouvel enregistrement ne soit engagé. Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**.

<table>
<colgroup>
<col style="width: 100%" />
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


Après que l'action **CréerEnregistrement** a créé un enregistrement, utilisez l'action **DéfinirChamp** pour spécifier une valeur d'un champ dans le nouvel enregistrement.

Vous pouvez utiliser une instruction **If... Then... Else** pour effectuer des opérations basées sur une condition.

Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**.

Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l’enregistrement. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement créé.

`[LastCreateRecordIdentity].[AssignedTo]`

Le bloc de données **CréerEnregistrement** peut être utilisé uniquement dans les événements de macros de données **[Après insertion](after-insert-macro-event.md)**, **[Après MAJ](after-update-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.

