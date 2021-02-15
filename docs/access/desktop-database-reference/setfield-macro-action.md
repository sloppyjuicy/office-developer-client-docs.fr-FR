---
title: SetField, action de macro
TOCTitle: SetField macro action
ms:assetid: 66bd26e3-e8c3-b9a1-2f16-f29adc44a345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195227(v=office.15)
ms:contentKeyID: 48545349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4fbf7252729c7b376da6ebe67f59941c1caf924d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314615"
---
# <a name="setfield-macro-action"></a>SetField, action de macro

**S’applique à** : Access 2013, Office 2013

L'action **DéfinirChamp** peut être utilisée pour assigner une valeur à un champ.

> [!NOTE]
> L’action **DéfinirChamp** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Setting

L’action **DéfinirChamp** utilise les arguments répertoriés dans le tableau suivant.

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
<td><p><strong>Name</strong></p></td>
<td><p>Chaîne qui identifie le champ.</p></td>
</tr>
<tr class="even">
<td><p><strong>Valeur</strong></p></td>
<td><p>Expression qui spécifie la valeur à affecter au champ.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'action **DéfinirChamp** ne peut pas être utilisée en dehors d'un bloc de données **[CréerEnregistrement](createrecord-data-block.md)** ou **[ModifierEnregistrement](editrecord-data-block.md)**.

