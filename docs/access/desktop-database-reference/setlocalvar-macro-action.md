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
ms.openlocfilehash: b257473d2acd3d17f30a3fdd579d213dcd39487b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996901"
---
# <a name="setlocalvar-macro-action"></a>SetLocalVar, action de macro

**S’applique à**: Access 2013, Office 2013

L'action **DéfinirVarLocale** crée une variable temporaire et lui affecte une valeur spécifique.

## <a name="setting"></a>Paramètre

L'action **DéfinirVarLocale** utilise les arguments suivants.

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
<td><p>Une expression qui sera utilisée pour définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression avec le signe égal (=). Vous pouvez cliquer sur le bouton <strong>Générer</strong> pour utiliser le <strong>Générateur d’Expression</strong> pour définir cet argument.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Notes

Les variables créées par l'action **DéfinirVarLocale** peuvent être utilisées uniquement dans la macro dans laquelle elles sont définies. Utilisez l'action **[DéfinirVarTemp](settempvar-macro-action.md)** pour définir une variable qui peut être utilisée dans une autre macro, dans une procédure événementielle ou dans un formulaire ou un état.

Une fois qu'une variable temporaire a été créée, vous pouvez la référencer dans une expression. Par exemple, si vous avez créé une variable temporaire nommée TotalAmount, vous pouvez l'utiliser comme source contrôle pour une zone de texte à l'aide de la syntaxe suivante.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> [!REMARQUE] Dans une macro de données, vous n'êtes pas obligé d'utiliser la collection LocalVars pour faire référence à une variable. Par exemple, si vous avez créé une variable temporaire dans une Macro de données nommée montant total, vous pouvez utiliser la variable comme source de contrôle pour une zone de texte à l’aide de la syntaxe suivante : `=[TotalAmount]`.

