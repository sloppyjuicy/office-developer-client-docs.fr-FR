---
title: SetTempVar, action de macro
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5e0d73c700acc66eaac40190012965d865c50b7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568480"
---
# <a name="settempvar-macro-action"></a>SetTempVar, action de macro


**S’applique à** : Access 2013, Office 2013



L'action **DéfinirVarTemp** permet de créer une variable temporaire et de la définir sur une valeur spécifique. La variable peut ensuite être utilisée en tant que condition ou argument dans les actions suivantes, dans une autre macro, dans une procédure événementielle, ou dans un formulaire ou un état.

## <a name="setting"></a>Paramètre

L’action **DéfinirVarTemp** utilise les arguments suivants :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>Entrez le nom de la variable temporaire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expression</strong></p></td>
<td><p>Expression qui permet de définir la valeur de cette variable temporaire. Ne faites pas précéder l’expression du signe <strong>=</strong> égal (). Vous pouvez cliquer sur le <strong>bouton</strong> Créer <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> pour utiliser le Générateur d’expression pour définir cet argument.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

- Vous pouvez définir jusqu'à 255 variables temporaires simultanément. Si vous ne supprimez pas une variable temporaire, elle reste en mémoire jusqu'à la fermeture de la base de données. Il est conseillé de supprimer les variables temporaires lorsque vous n'en avez plus besoin. Pour supprimer une variable temporaire unique, utilisez l'action **[SupprimerVarTemp](removetempvar-macro-action.md)** et définissez son argument sur le nom de la variable temporaire à supprimer. Pour supprimer plusieurs variables temporaires en une opération, utilisez l'action **SupprimerToutesVarTemp**.

- Les variables temporaires sont des variables globales. Après la création d'une variable temporaire, vous pouvez y faire référence dans une procédure événementielle, un module Visual Basic pour Applications (VBA), une requête ou une expression. Par exemple, si vous avez créé une variable temporaire nommée *MyVar*, vous pouvez utiliser la variable comme source de contrôle pour une zone de texte à l’aide de la syntaxe suivante :
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > [!REMARQUE] Dans les macros, requêtes et procédures événementielles, il n'est pas nécessaire d'insérer un signe égal devant l'expression.
 
  Vous pouvez également faire référence aux variables temporaires dans les compléments ou les bases de données référencées.

- Pour exécuter l’action **DéfinirVarTemp** dans un module VBA, utilisez la méthode **Add** de l’objet **TempVars**.

## <a name="example"></a>Exemple

La macro suivante explique comment créer une variable temporaire, en utilisant d’abord l’action **DéfinirVarTemp**, puis la variable temporaire dans une condition et une boîte de message et, enfin, en supprimant la variable temporaire.

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
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]![MaVar] &lt;&gt;0</p></td>
<td><p><strong>MessageBox</strong></p></td>
<td><p><strong>Message</strong>: = &quot; vous avez entré &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveTempVar</strong></p></td>
<td><p><strong>Nom</strong>: MaVar</p></td>
</tr>
</tbody>
</table>

