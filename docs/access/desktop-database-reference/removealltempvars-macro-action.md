---
title: SupprimerToutesVarTemp, action de macro
TOCTitle: RemoveAllTempVars Macro Action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 42217fea05b29fdf127945d1547adbac28346cc9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470578"
---
# <a name="removealltempvars-macro-action"></a>SupprimerToutesVarTemp, action de macro


**S’applique à**: Access 2013 | Office 2013


L'action **SupprimerToutesVarTemp** permet de supprimer toutes les variables temporaires que vous avez créées en utilisant l'action **DéfinirVarTemp**.

## <a name="setting"></a>Paramètre

L'action **SupprimerToutesVarTemp** ne possède aucun argument.

## <a name="remarks"></a>Notes

  - Vous pouvez définir jusqu'à 255 variables temporaires à la fois. Toute variable temporaire non supprimée reste en mémoire jusqu'à ce que la base de données ou le projet soit fermé. Il est conseillé de supprimer les variables temporaires lorsque vous ne les utilisez plus.

  - Access supprime automatiquement toutes les variables temporaires lorsque vous fermez la base de données ou le projet.

  - Pour supprimer une seule variable temporaire, utilisez l'action **SupprimerVarTemp** et définissez son argument sur le nom de la variable temporaire que vous souhaitez supprimer.

  - Pour exécuter l'action **SupprimerToutesVarTemp** dans un module VBA, utilisez la méthode **RemoveAll** de l'objet **TempVars**.

## <a name="example"></a>Exemple

La macro suivante illustre comment créer une variable temporaire, l'utiliser dans une condition et une zone de message, puis la supprimer en utilisant l'action **SupprimerToutesVarTemp**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p><strong>DéfinirVarTemp</strong></p></td>
<td><p><strong>Nom</strong>: MaVar<strong>Expression</strong>: BEntrée (&quot;Entrez un nombre différent de zéro.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MaVar] &lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: =&quot;vous avez entré &quot; &amp; [VarTemp] ! [MaVar] &amp; &quot;. &quot; <strong>Bip</strong>: <strong>YesType</strong>: <strong>informations</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SupprimerToutesVarTemp</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

