---
title: DROP USER ou GROUP, instruction (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293643"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER ou GROUP, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Supprime un ou plusieurs *utilisateurs* ou *groupes*existants, ou supprime un ou plusieurs *utilisateurs* existants d'un *groupe*existant.

## <a name="syntax"></a>Syntaxe

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Supprimer un ou plusieurs utilisateurs ou supprimer un ou plusieurs utilisateurs d'un groupe

Drop user **\[User, *User*,... \] du *groupe* \[\]

### <a name="delete-one-or-more-groups"></a>Supprimer un ou plusieurs groupes

Drop Group **\[Group, *Group*,...\]

L'instruction DROP USER ou GROUP est composée des arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Élément</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>utilisateur</em></p></td>
<td><p>Nom de l'utilisateur à supprimer du fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="even">
<td><p><em>groupe</em></p></td>
<td><p>Nom du groupe à supprimer du fichier d'informations du groupe de travail.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Si le mot clé FROM est utilisé dans l'instruction DROP USER, chacun des *utilisateurs* figurant dans l'instruction est supprimé du *groupe* spécifié à la suite du mot clé from. Toutefois, les *utilisateurs* eux-mêmes ne seront pas supprimés.

L'instruction DROP GROUP supprime les *groupes* spécifiés. Les *utilisateurs* qui sont membres du ou des *groupes*ne seront pas affectés, mais ils ne seront plus membres du ou des *groupes*supprimés.

