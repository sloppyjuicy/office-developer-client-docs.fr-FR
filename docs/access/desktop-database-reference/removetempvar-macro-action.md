---
title: RemoveTempVar, action de macro
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 224cd6072ad615792736304c7a2956a8b3a06816
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63725869"
---
# <a name="removetempvar-macro-action"></a>RemoveTempVar, action de macro


**S’applique à** : Access 2013, Office 2013



L’action **SupprimerVarTemp** permet de supprimer une seule variable temporaire que vous avez créée en utilisant l’action **DéfinirVarTemp**.

## <a name="setting"></a>Setting

L’action **SupprimerVarTemp** possède l’argument suivant.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Name</strong></p></td>
<td><p>Entrez le nom de la variable temporaire que vous souhaitez supprimer.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

  - Vous pouvez définir jusqu'à 255 variables temporaires à la fois. Toute variable temporaire non supprimée reste en mémoire jusqu'à ce que la base de données soit fermée. Il est conseillé de supprimer les variables temporaires lorsque vous ne les utilisez plus.

  - Access supprime automatiquement toutes les variables temporaires lorsque vous fermez la base de données ou le projet.

  - Si le nom de la variable à supprimer est mal orthographié, Access n'affiche aucun message d'erreur. La variable concernée est conservée en mémoire tant que vous ne fermez pas la base de données.

  - Si vous avez créé plusieurs variables temporaires et souhaitez toutes les supprimer en une fois, utilisez l'action **SupprimerToutesVarTemp**.

  - Pour exécuter l’action **SupprimerVarTemp** dans un module VBA, utilisez la méthode **Remove** de l’objet **TempVars**.

## <a name="example"></a>Exemple

La macro suivante illustre comment créer une variable temporaire, l'utiliser dans une condition et une zone de message, puis la supprimer en utilisant l'action **SupprimerVarTemp**.

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
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Nom</strong>: MaVar</p></td>
</tr>
</tbody>
</table>

