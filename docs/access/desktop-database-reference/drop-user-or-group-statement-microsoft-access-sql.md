---
title: DROP USER ou GROUP, instruction (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fcfb1c225e8e5bb202eb64cfeff84ea1f7f9ba55
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628823"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a>DROP USER ou GROUP, instruction (Microsoft Access SQL)

**S’applique à** : Access 2013, Office 2013

Supprime un ou plusieurs utilisateurs *ou groupes* existants *ou supprime* un ou plusieurs utilisateurs existants  d’un groupe *existant*.

## <a name="syntax"></a>Syntaxe

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a>Supprimer un ou plusieurs utilisateurs ou supprimer un ou plusieurs utilisateurs d’un groupe

DROP USER *user*\[, *user*, ...\] \[ Groupe *FROM*\]

### <a name="delete-one-or-more-groups"></a>Supprimer un ou plusieurs groupes

DROP GROUP *group*\[, *group*, ...\]

L'instruction DROP USER ou GROUP est composée des arguments suivants :

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Quitter</p></th>
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

Si le mot clé FROM est utilisé dans l’instruction DROP USER, chacun  des utilisateurs répertoriés dans l’instruction est supprimé du  groupe spécifié à la suite du mot clé FROM. Toutefois, les *utilisateurs* eux-mêmes ne seront pas supprimés.

L'instruction DROP GROUP supprime les *groupes* spécifiés. Les *utilisateurs* qui sont membres *du ou des* groupes ne seront pas affectés, mais ils ne seront plus membres *du ou des* groupes supprimés.

