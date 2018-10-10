---
title: Avant la suppression, événement de macro
TOCTitle: Before Delete Macro Event
ms:assetid: 1a8d3457-5c59-d13e-ada9-6ecd33dfd5b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845672(v=office.15)
ms:contentKeyID: 48543520
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm186077
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7863f8500a81014f3c70b5547fb363c46803f4f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471336"
---
# <a name="before-delete-macro-event"></a>Avant la suppression, événement de macro

**S’applique à**: Access 2013 | Office 2013

L'événement **Avant la suppression** se produit lorsqu'un enregistrement est supprimé, mais avant la validation de la modification.

> [!NOTE]
> [!REMARQUE] L'événement **Avant la suppression** est disponible uniquement dans les macros de données.

## <a name="remarks"></a>Notes

Utilisez l'événement **Avant la suppression** pour effectuer toute action souhaitée avant qu'un enregistrement soit modifié. **Avant la modification** s'utilise couramment pour effectuer une validation et pour déclencher des messages d'erreur personnalisés.

Vous pouvez accéder à une valeur dans l’enregistrement à supprimer à l’aide de la syntaxe suivante :

`[Old].[Field Name]`

Par exemple, pour accéder à la valeur du champ QuantityInStock dans l’enregistrement à supprimer, utilisez la syntaxe suivante :

`[Old].[QuantityInStock]`

Les valeurs contenues dans l'enregistrement à supprimer sont supprimées définitivement lorsque l'événement **Avant la suppression** se termine.

Vous pouvez annuler l'événement **Avant la suppression** à l'aide de l'action **DéclencherErreur**. Lorsqu’une erreur se produit, les modifications contenues dans l’événement **Avant la suppression** sont ignorées.

Le tableau suivant répertorie les commandes de macros qui peuvent être utilisées dans l'événement **Avant la suppression**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de commande</p></th>
<th><p>Commande</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Déroulement de programme</p></td>
<td><p><a href="comment-macro-statement.md">Comment, instruction de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Déroulement de programme</p></td>
<td><p><a href="group-macro-statement.md">Group, instruction de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Déroulement de programme</p></td>
<td><p><a href="if-then-else-macro-block.md">If...Then...Else, bloc de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Bloc de données</p></td>
<td><p><a href="lookuprecord-data-block.md">Action de Macro RechercherEnregistrement</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="clearmacroerror-macro-action.md">EffacerMacroErreur, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="onerror-macro-action.md">SurErreur, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="raiseerror-macro-action.md">DéclencherErreur, action de macro</a></p></td>
</tr>
<tr class="even">
<td><p>Action de données</p></td>
<td><p><a href="setlocalvar-macro-action.md">DéfinirVarLocale, action de macro</a></p></td>
</tr>
<tr class="odd">
<td><p>Action de données</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></p></td>
</tr>
</tbody>
</table>


Pour créer une macro de données qui capture l'événement **Avant la suppression**, procédez comme suit.

1.  Ouvrez la table pour laquelle vous souhaitez capturer l'événement **Avant la suppression**.

2.  Sous l’onglet **Table** , dans le groupe **Événements avant** , sélectionnez **Avant la suppression**.

