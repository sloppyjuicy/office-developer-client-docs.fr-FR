---
title: Group, instruction de macro
TOCTitle: Group Macro Statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35f9ad1d445dbddaa5487e28da60b9202a72dae1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879850"
---
# <a name="group-macro-statement"></a>Group, instruction de macro


**S’applique à**: Access 2013, Office 2013

L’instruction **Group** vous permet de spécifier un bloc d’actions dans une macro que vous pouvez développer ou réduire.

## <a name="setting"></a>Paramètre

L'instruction **Group** utilise les arguments suivants.

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
<td><p><strong>Description</strong></p></td>
<td><p>Non</p></td>
<td><p>Chaîne qui s’affiche comme titre d’un groupe lorsqu’il est réduit.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'instruction **Group** ne définit pas une région d'une macro qui peut être exécutée séparément. Utilisez l'instruction **[Submacro](submacro-macro-statement.md)** pour définir un ensemble d'actions à exécuter séparément dans la fenêtre **Concepteur de macros**.

