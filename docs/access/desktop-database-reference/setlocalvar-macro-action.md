---
title: SetLocalVar, action de macro
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314587"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar, action de macro

**S’applique à** : Access 2013, Office 2013

Le **DéfinirVarLocale** action crée une variable temporaire et définissez-la sur une valeur spécifique.

## <a name="setting"></a>Paramètre

L’action **DéfinirVarTemp** utilise les arguments suivants :

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
<td><p><strong>Name</strong></p></td>
<td><p>Oui</p></td>
<td><p>Chaîne qui spécifie le nom de la variable.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Oui</p></td>
<td><p>Expression destiné à être utilisé pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression d’un signe égal (=). Vous pouvez cliquer sur le bouton <strong>Générer</strong> afin d’utiliser le <strong>Générateur d’expressions</strong> pour définir cet argument.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Variables créés par le **DéfinirVarLocale** action peut être utilisée uniquement dans la macro dans lequel ils sont définis. Utilisez le ** [DéfinirVarTemp](settempvar-macro-action.md) ** action pour définir une variable qui peut être utilisée dans une autre macro dans une procédure événementielle ou dans un formulaire ou état.

Une fois une variable temporaire a été créée, vous pouvez la consulter dans une expression. Par exemple, si vous avez créé une variable temporaire nommée TotalAmount, vous pouvez l’utiliser comme source contrôle pour une zone de texte à l’aide de la syntaxe suivante.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> Dans une macro de données, vous devez ne pas utiliser la collection VarLocale pour faire référence à une variable. Par exemple, si vous avez créé une variable temporaire dans une macro de données nommée TotalAmount, vous pouvez utiliser la variable comme source contrôle pour une zone de texte à l’aide de la syntaxe suivante : `=[TotalAmount]`.

