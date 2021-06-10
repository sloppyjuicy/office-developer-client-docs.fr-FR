---
title: SetOrderBy, action de macro
TOCTitle: SetOrderBy macro action
ms:assetid: 78f65ce9-b56f-f476-3bd6-f3307bc22a08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196152(v=office.15)
ms:contentKeyID: 48545765
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98639
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 86834cd8b6132e8939067c0e34037ca1b0ef8bad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314608"
---
# <a name="setorderby-macro-action"></a>SetOrderBy, action de macro


**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l’action **DéfinirOrdrePar** pour spécifier comment vous souhaitez trier les enregistrements d’un formulaire, d’un état, d’une table ou d’un résultat de requête.

## <a name="setting"></a>Paramètre

L’action **DéfinirOrdrePar** utilise les arguments suivants.

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
<td><p><strong>Trier par</strong></p></td>
<td><p>Expression de type Chaîne qui inclut le nom des champs sur lesquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nom du contrôle</strong></p></td>
<td><p>S’il est fourni et que l’objet actif est un formulaire ou un état, il s’agit du nom du contrôle qui correspond au sous-formulaire ou sous-état qui sera trié. Si l’argument est vide et que l’objet actif est un formulaire ou un état, le formulaire ou l’état parent est trié.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Lorsque vous exécutez cette action de macro, le tri est appliqué à la table, au formulaire, à l'état ou à la feuille de données (résultat de la requête) qui est actif et qui a le focus.

L'argument Trier par est le nom des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,). La propriété **TriPar** de l'objet actif est utilisée pour enregistrer la valeur de tri et l'appliquer ultérieurement. Les valeurs de TriPar sont enregistrées avec les objets dans lesquels elles sont créées. Elles sont chargées automatiquement lors de l'ouverture de l'objet, mais elles ne sont pas appliquées automatiquement.

Lorsque vous définissez l'argument Trier par en entrant un ou plusieurs noms de champs et que vous exécutez ensuite la macro, les enregistrements sont triés par défaut dans l'ordre croissant.

Pour trier les enregistrements par ordre décroissant, tapez DESC à la fin de l'expression d'argument Trier par. Par exemple, pour trier des enregistrements clients par ordre décroissant par nom de contact, affectez à l'argument Trier par la valeur « NomContact DESC ». Pour trier les noms par Nom décroissant et Prénom croissant, affectez à l'argument Trier par la valeur « Nom DESC, Prénom ASC ».

