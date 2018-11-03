---
title: Instruction DROP USER ou GROUP (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f9662c4f0cb691136a556faa32cb0d5a1c775268
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936832"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>Instruction DROP USER ou GROUP (Microsoft Access SQL)

**S’applique à**: Access 2013, Office 2013

Supprime un ou plusieurs *utilisateurs* ou *groupes*, ou un ou plusieurs *utilisateurs* existants à partir d’un *groupe*existant.

## <a name="syntax"></a>Syntaxe

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Supprimer un ou plusieurs utilisateurs ou supprimer un ou plusieurs utilisateurs d’un groupe

DROP USER *utilisateur*\[, *utilisateur*,... \] \[De *groupe*\]

### <a name="delete-one-or-more-groups"></a>Supprimer un ou plusieurs groupes

DROP GROUP *groupe*\[, *groupe*,...\]

L'instruction DROP USER ou GROUP est composée des arguments suivants :

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
<td><p><em>utilisateur</em></p></td>
<td><p>Nom de l'utilisateur à supprimer du fichier d'informations du groupe de travail.</p></td>
</tr>
<tr class="even">
<td><p><em>Groupe</em></p></td>
<td><p>Nom du groupe à supprimer du fichier d'informations du groupe de travail.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Si le mot clé FROM est utilisé dans l’instruction DROP USER, chacun des *utilisateurs* figurant dans l’instruction sera supprimé du *groupe* spécifié après le mot clé FROM. Toutefois, les *utilisateurs* eux-mêmes ne seront pas supprimés.

L’instruction DROP GROUP supprimera spécifié *groupe*(s). Les *utilisateurs* qui sont membres du *groupe*(s) ne seront pas affectés, mais ils ne seront plus membres supprimés de *groupe (s)*.

