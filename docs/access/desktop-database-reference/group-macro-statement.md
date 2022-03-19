---
title: Group, instruction de macro
TOCTitle: Group macro statement
ms:assetid: 42aa4afa-ab5d-9dcc-2182-786f025e316d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192918(v=office.15)
ms:contentKeyID: 48544481
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1e7e8750dfee6eaec14117d5782367ddd76cc622
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63634253"
---
# <a name="group-macro-statement"></a>Group, instruction de macro


**S’applique à** : Access 2013, Office 2013

**L’instruction** Group vous permet de spécifier un bloc d’actions dans une macro que vous pouvez développer ou réduire.

## <a name="setting"></a>Paramètres

L’instruction **Group** utilise les arguments suivants.

<table>
<colgroup>
<col />
<col />
<col />
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


## <a name="remarks"></a>Remarques

L'instruction **Group** ne définit pas une région d'une macro qui peut être exécutée séparément. Utilisez l'instruction **[Submacro](submacro-macro-statement.md)** pour définir un ensemble d'actions à exécuter séparément dans la fenêtre **Concepteur de macros**.

