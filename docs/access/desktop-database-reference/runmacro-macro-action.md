---
title: ExécuterMacro, action de macro
TOCTitle: RunMacro Macro Action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 533ac6aff194296a9e4470e01672a8338dcbc318
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472198"
---
# <a name="runmacro-macro-action"></a>ExécuterMacro, action de macro


**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l'action **ExécuterMacro** pour exécuter une macro. La macro peut faire partie d'un groupe de macros.

Vous pouvez utiliser cette action dans les cas suivants :

  - Pour exécuter une macro à partir d'une autre macro.

  - Pour exécuter une macro en fonction d'une condition définie.

  - Pour attacher une macro à une commande de menu personnalisée.

## <a name="setting"></a>Valeur

L'action **ExécuterMacro** accepte les arguments suivants.

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
<td><p>Nom de la macro à exécuter. La zone <strong>Nom de la Macro</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro affiche toutes les macros (et groupes de macros) dans la base de données en cours. Si la macro est dans un groupe de macros, elle est répertoriée sous le nom du groupe de macros dans la liste en tant que <em>nomgroupemacros</em>. <em>nommacro</em>. Cet argument est obligatoire. Si vous exécutez une macro contenant l’action <strong>ExécuterMacro</strong> dans une base de données bibliothèque, Microsoft Access recherche la macro portant ce nom dans la base de données bibliothèque, et non pas dans la base de données active.</p></td>
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


## <a name="remarks"></a>Notes

Si vous entrez le nom d'un groupe de macros dans l'argument **Nom de macro**, Access exécute la première macro du groupe.

Pour l'essentiel, cette action équivaut à cliquer sur le bouton **Exécuter une macro** dans l'onglet **Outils de base de données**, à sélectionner une macro, puis à cliquer sur **OK**. Toutefois, cette commande n'exécute la macro qu'une seule fois tandis que l'action **ExécuterMacro** permet d'exécuter une macro autant de fois que vous le souhaitez.


> [!TIP]
> <P>[!CONSEIL] Vous pouvez utiliser les arguments <STRONG>Nombre de répétitions</STRONG> et <STRONG>Expression de répétition</STRONG> pour déterminer le nombre de fois que la macro doit s'exécuter :</P>



  - Si vous laissez les deux arguments vides, la macro s'exécute une seule fois.

  - Si vous entrez un nombre dans la zone de l'argument **Répéter compte** et que vous ne spécifiez rien pour l'argument **Répéter expression**, la macro s'exécute le nombre de fois spécifié.

  - Si vous ne spécifiez rien pour **Répéter compte** et que vous entrez une expression dans la zone **Répéter expression**, la macro s'exécute jusqu'à ce que l'expression corresponde à **Faux**.

  - Si vous spécifiez des valeurs pour les deux arguments, la macro s'exécute le nombre de fois spécifié dans **Répéter compte** ou jusqu'à ce que **Répéter expression** corresponde à **Faux**, selon la valeur atteinte en premier.

Lorsque vous exécutez une macro contenant l'action **ExécuterMacro** et qu'elle atteint l'action **ExécuterMacro**, Access exécute la macro appelée. Lorsque la macro appelée a terminé de s'exécuter, Access retourne à la macro d'origine et exécute l'action suivante.


> [!NOTE]
> <UL>
> <LI>
> <P>Vous pouvez appeler une macro du même groupe de macros ou d'un autre groupe de macros.</P>
> <LI>
> <P>Vous pouvez imbriquer les macros. En d'autres termes, vous pouvez exécuter la macro A qui appelle à son tour la macro B, et ainsi de suite. Dans chaque cas, lorsque la macro appelée est terminée, Access retourne à la macro qui l'a appelée et exécute l'action suivante dans la macro.</P></LI></UL>



Pour exécuter l'action **ExécuterMacro** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **RunMacro** de l'objet **DoCmd**.

