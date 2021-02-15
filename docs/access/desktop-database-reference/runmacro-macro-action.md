---
title: RunMacro, action de macro
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d9e86fb7d60af94d6ecde71b2a857a3cc5b9bcb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306852"
---
# <a name="runmacro-macro-action"></a>RunMacro, action de macro

**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser l'action **ExécuterMacro** pour exécuter une macro. La macro peut faire partie d'un groupe de macros.

Vous pouvez utiliser cette action dans les cas suivants :

- Pour exécuter une macro à partir d'une autre macro.

- Pour exécuter une macro en fonction d'une condition définie.

- Pour attacher une macro à une commande de menu personnalisée.

## <a name="setting"></a>Setting

L’action **ExécuterMacro** accepte les arguments suivants.

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
<td><p><strong>Nom macro</strong></p></td>
<td><p>Nom de la macro à exécuter. La <strong>zone Nom de</strong> macro de la section Arguments de l’action du volet Générateur de macro affiche toutes les macros (et groupes de macros) de la base de données actuelle. <strong></strong> Si la macro se trouve dans un groupe de macros, elle est répertoriée sous le nom du groupe de macros dans la liste en tant que <em>nom de groupe de macros.</em> <em>nom_macro</em>. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>ExécuterMacro</strong> dans une base de données bibliothèque, Microsoft Access recherche la macro portant ce nom dans la base de données bibliothèque, et non pas dans la base de données active.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre de répétitions</strong></p></td>
<td><p>Nombre maximal d’exécutions de la macro. Si vous laissez cet argument vide (et que l’argument <strong>Expression de répétition</strong> est également vide), la macro s’exécute une seule fois.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expression de répétition</strong></p></td>
<td><p>Expression qui renvoie <strong>Vrai</strong> (–1) ou <strong>Faux</strong> (0). La macro arrête de s’exécuter si l’expression renvoie <strong>Faux</strong>. Cette expression est évaluée à chaque exécution de la macro.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Remarques

Si vous entrez le nom d’un groupe de macros dans l’argument **Nom de macro**, Access exécute la première macro du groupe.

Pour l'essentiel, cette action équivaut à cliquer sur le bouton **Exécuter une macro** dans l'onglet **Outils de base de données**, à sélectionner une macro, puis à cliquer sur **OK**. Toutefois, cette commande n'exécute la macro qu'une seule fois tandis que l'action **ExécuterMacro** permet d'exécuter une macro autant de fois que vous le souhaitez.

> [!TIP]
> [!CONSEIL] Vous pouvez utiliser les arguments **Nombre de répétitions** et **Expression de répétition** pour déterminer le nombre de fois que la macro doit s'exécuter :
> - Si vous laissez les deux arguments vides, la macro s'exécute une seule fois.
> - Si vous entrez un nombre dans la zone de l'argument **Répéter compte** et que vous ne spécifiez rien pour l'argument **Répéter expression**, la macro s'exécute le nombre de fois spécifié.
> - Si vous ne spécifiez rien pour **Répéter compte** et que vous entrez une expression dans la zone **Répéter expression**, la macro s'exécute jusqu'à ce que l'expression corresponde à **Faux**.
> - Si vous spécifiez des valeurs pour les deux arguments, la macro s'exécute le nombre de fois spécifié dans **Répéter compte** ou jusqu'à ce que **Répéter expression** corresponde à **Faux**, selon la valeur atteinte en premier.

Lorsque vous exécutez une macro contenant l'action **ExécuterMacro** et qu'elle atteint l'action **ExécuterMacro**, Access exécute la macro appelée. Lorsque la macro appelée a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.

> [!NOTE]
> - Vous pouvez appeler une macro du même groupe de macros ou d'un autre groupe de macros.
> - Vous pouvez imbriquer les macros. En d'autres termes, vous pouvez exécuter la macro A qui appelle à son tour la macro B, et ainsi de suite. Dans chaque cas, lorsque la macro appelée est terminée, Access retourne à la macro qui l'a appelée et exécute l'action suivante dans la macro.

Pour exécuter l'action **ExécuterMacro** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RunMacro** de l'objet **DoCmd**.

