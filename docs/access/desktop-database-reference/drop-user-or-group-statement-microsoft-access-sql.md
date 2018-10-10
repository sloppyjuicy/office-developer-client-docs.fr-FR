---
title: DROP USER ou GROUP, instruction (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469604"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER ou GROUP, instruction (Microsoft Access SQL)


**S’applique à**: Access 2013 | Office 2013

Supprime un ou plusieurs *utilisateurs* ou *groupes* existants ou un ou plusieurs *utilisateurs* d'un *groupe* existant.

## <a name="syntax"></a>Syntaxe

Supprimer un ou plusieurs *utilisateurs* ou supprimer un ou plusieurs *utilisateurs* d'un *groupe*:

DROP USER *utilisateur*\[, *utilisateur*,... \] \[De *groupe*\]

Supprimer un ou plusieurs *groupes* :

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

Si le mot clé FROM est utilisé dans l'instruction DROP USER, alors chacun des *utilisateurs* indiqué dans l'instruction est supprimé du *groupe* spécifié à la suite du mot clé FROM. En revanche, les *utilisateurs* eux-mêmes ne sont pas supprimés.

L'instruction DROP GROUP supprime les *groupes* spécifiés. Les *utilisateurs* qui sont membres des *groupes* ne sont pas supprimés, mais ils ne sont plus membres des *groupes* supprimés.

