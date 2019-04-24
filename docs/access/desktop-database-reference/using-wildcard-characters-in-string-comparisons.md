---
title: Utilisation de caractères génériques dans les comparaisons de chaînes
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6a013865b9615701b1d99678fc2392e0a896c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305935"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Utilisation de caractères génériques dans les comparaisons de chaînes

**S’applique à** : Access 2013, Office 2013

La fonction intégrée de recherche des correspondances de chaînes constitue un outil polyvalent permettant de comparer des chaînes. Le tableau suivant montre les caractères génériques que vous pouvez utiliser avec l'opérateur **Like** ainsi que les chiffres ou les chaînes auxquels ils correspondent.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Caractère(s) dans <em>motif</em></p></th>
<th><p>Correspondances dans <em>expression</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? ou _ (caractère de soulignement)</p></td>
<td><p>Un seul caractère</p></td>
</tr>
<tr class="even">
<td><p>*des</p></td>
<td><p>Zéro, un ou plusieurs caractères</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Tout chiffre isolé (0 à 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>charlist</em>]</p></td>
<td><p>Tout caractère isolé trouvé dans <em>listecar</em></p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p>Tout caractère isolé non trouvé dans <em>listecar</em></p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser un groupe d'un ou de plusieurs caractères (*listecar*) placés entre crochets\[ \]() pour faire correspondre tout caractère unique dans *expression,* et *listecar* peut inclure tous les caractères du jeu de caractères ANSI, y compris numérique. Vous pouvez utiliser le crochet ouvrant (\[ ), le point d'interrogation (?), le signe\#dièse () et l'\*astérisque () pour qu'ils correspondent directement uniquement s'ils sont entourés de crochets. Vous ne pouvez pas utiliser le crochet \]fermant () au sein d'un groupe pour qu'il corresponde à lui-même, mais vous pouvez l'utiliser en dehors d'un groupe en tant que caractère individuel.

Outre une simple liste de caractères encadrée par des crochets, *listecar* peut spécifier une plage de caractères en utilisant un tiret (-) pour séparer la borne supérieure et la borne inférieure de la plage. Par exemple, l' \[utilisation de A\] -Z dans *pattern* se traduit par une correspondance si la position du caractère correspondante dans *expression* contient l'une des lettres majuscules comprises entre A et Z. Vous pouvez inclure plusieurs plages entre les crochets sans délimiter les plages. Par exemple, \[a-zA-z0-9\] correspond à n'importe quel caractère alphanumérique.

Il est important de noter que les caractères génériques ANSI SQL (%) et (\_) sont disponibles uniquement avec Microsoft Jet version 4. X et le fournisseur Microsoft OLE DB pour jet. Ils sont interprétés comme des caractères littéraux lors de l'utilisation avec Microsoft Access ou DAO.

Les autres règles importantes en matière de correspondance de chaîne sont les suivantes :

- Un point d'exclamation\!() au début de *listecar* signifie qu'une correspondance est trouvée si un caractère quelconque, sauf ceux de *charlist* , se trouve dans *expression*. Utilisé hors des crochets, le point d'exclamation se recherche lui-même..

- Vous pouvez utiliser le tiret (-) au début (après un point d'exclamation s'il y en a un) ou à la fin de *listecar* pour qu'il se recherche lui-même. Placé à tout autre endroit, le tiret sert à identifier une plage de caractères ANSI

- Lorsque vous spécifiez une plage de caractères, ces derniers doivent apparaître en ordre ascendant (A-Z ou 0-100). \[A-Z\] est un modèle valide, mais \[Z-a\] ne l'est pas.

- La séquence \[ \] de caractères est ignorée; elle est considérée comme une chaîne de longueur nulle ("").

