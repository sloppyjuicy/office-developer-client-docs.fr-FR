---
title: RemoveAllTempVars, action de macro
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 02066ea7b62a8d9325f1687c159b1df78ee8e734
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63724885"
---
# <a name="removealltempvars-macro-action"></a>RemoveAllTempVars, action de macro


**S’applique à** : Access 2013, Office 2013


L’action **SupprimerToutesVarTemp** permet de supprimer toutes les variables temporaires que vous avez créées en utilisant l’action **DéfinirVarTemp**.

## <a name="setting"></a>Setting

L’action **SupprimerToutesVarTemp** ne possède aucun argument.

## <a name="remarks"></a>Remarques

  - Vous pouvez définir jusqu'à 255 variables temporaires à la fois. Toute variable temporaire non supprimée reste en mémoire jusqu'à ce que la base de données ou le projet soit fermé. Il est conseillé de supprimer les variables temporaires lorsque vous ne les utilisez plus.

  - Access supprime automatiquement toutes les variables temporaires lorsque vous fermez la base de données ou le projet.

  - Pour supprimer une seule variable temporaire, utilisez l'action **SupprimerVarTemp** et définissez son argument sur le nom de la variable temporaire que vous souhaitez supprimer.

  - Pour exécuter l'action **SupprimerToutesVarTemp** dans un module VBA, utilisez la méthode **RemoveAll** de l'objet **TempVars**.

## <a name="example"></a>Exemple

La macro suivante illustre comment créer une variable temporaire, l'utiliser dans une condition et une zone de message, puis la supprimer en utilisant l'action **SupprimerToutesVarTemp**.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Action</p></th>
<th><p>Arguments</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Name</strong>: <strong>MyVarExpression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MaVar] &lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong> : =&quot;Vous avez entré &quot; &amp; [TempVars]![ MyVar] &amp; &quot;.&quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

