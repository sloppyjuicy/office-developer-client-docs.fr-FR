---
title: DeleteRecord, action de macro
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 052e7a489eaec526db1552ced89b095f65f652df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921585"
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

