---
title: DeleteRecord, action de macro
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725951"
---
# <a name="deleterecord-macro-action"></a>DeleteRecord, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **SupprimerEnregistrement** pour supprimer un enregistrement.

## <a name="setting"></a>Paramètre

Le bloc de données **SupprimerEnregistrement** utilise les arguments suivants.

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
<td><p><strong>Alias d’enregistrement</strong></p></td>
<td><p>Chaîne qui identifie l’enregistrement à supprimer. Si l’argument <em>Alias</em> n’est pas spécifié, l’enregistrement actif est supprimé.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Notes

Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence à l’enregistrement plus récent :

`[LastCreateRecordIdentity]`

