---
title: Utilisation de caractères génériques dans les comparaisons de chaînes
TOCTitle: Using wildcard characters in string comparisons
ms:assetid: 37dda2b8-c710-4f73-bb2a-76a1348c42fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192499(v=office.15)
ms:contentKeyID: 48544205
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fb6c63d5d2db1db54d52a03fef41e44a29f42c9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026162"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a>Utilisation de caractères génériques dans les comparaisons de chaînes

**S’applique à**: Access 2013, Office 2013

La fonction intégrée de recherche des correspondances de chaînes constitue un outil polyvalent permettant de comparer des chaînes. Le tableau suivant montre les caractères génériques que vous pouvez utiliser avec l'opérateur **Like** ainsi que les chiffres ou les chaînes auxquels ils correspondent.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Caractère (s) dans <em>motif</em></p></th>
<th><p>Correspondances dans <em>expression</em></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>? ou _ (caractère de soulignement)</p></td>
<td><p>Tout caractère isolé</p></td>
</tr>
<tr class="even">
<td><p>*ou %</p></td>
<td><p>Zéro, un ou plusieurs caractères</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Tout chiffre isolé (0 à 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>listecar</em>]</p></td>
<td><p>Tout caractère unique dans <em>charlist</em></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>listecar</em>]</p></td>
<td><p>Tout caractère unique non trouvé dans <em>listecar</em></p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser un groupe d’un ou plusieurs caractères (*argument charlist*) placés entre crochets (\[ \]) pour faire correspondre tout caractère unique dans *expression,* sachant que *listecar* peut inclure tous les caractères dans le caractère ANSI défini, y compris chiffres. Vous pouvez utiliser les caractères spéciaux crochet ouvrant (\[ ), point d’interrogation (?), le signe dièse (\#) et l’astérisque (\*) pour faire référence à eux-mêmes uniquement si entre crochets. Vous ne pouvez pas utiliser le crochet fermant ( \]) au sein d’un groupe pour correspondre à lui-même, mais vous pouvez l’utiliser en dehors d’un groupe de caractères.

Outre une simple liste de caractères placés entourés crochets, *charlist* peut spécifier une plage de caractères à l’aide d’un trait d’union (-) pour séparer les deux et les limites inférieures de la plage. Par exemple, à l’aide de \[A-Z\] dans *pattern, une correspondance si la position du caractère correspondant dans *expression* contient une lettre majuscule dans la plage de A à Z* . Vous pouvez inclure plusieurs plages entre les crochets sans les délimiter. Par exemple, \[a-zA-Z0-9\] correspond à n’importe quel caractère alphanumérique.

Il est important de noter que les caractères génériques SQL ANSI (%) et (\_) sont uniquement disponibles avec Microsoft Jet version 4.X et le fournisseur Microsoft OLE DB pour Jet. Ils sont interprétés comme des caractères littéraux lors de l'utilisation avec Microsoft Access ou DAO.

Les autres règles importantes en matière de correspondance de chaîne sont les suivantes :

- Un point d’exclamation (\!) au début de *charlist* signifie que la correspondance est établie si tout caractère sauf ceux présents dans *listecar* sont trouve dans *expression*. Utilisé hors des crochets, le point d'exclamation se recherche lui-même..

- Vous pouvez utiliser le trait d’union (-) au début (après un point d’exclamation si elle est utilisée) ou à la fin de *l’argument charlist* pour correspondre à lui-même. Placé à tout autre endroit, le tiret sert à identifier une plage de caractères ANSI

- Lorsque vous spécifiez une plage de caractères, ces derniers doivent apparaître en ordre ascendant (A-Z ou 0-100). \[A-Z\] est un modèle valide, mais \[Z-A\] n’est pas.

- La séquence de caractères \[ \] est ignorée ; elle est considérée comme une chaîne de longueur nulle ( » »).

