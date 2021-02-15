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
<td><p>* ou %</p></td>
<td><p>Zéro, un ou plusieurs caractères</p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p>Tout chiffre isolé (0 à 9)</p></td>
</tr>
<tr class="even">
<td><p>[<em>liste de listes</em>]</p></td>
<td><p>Tout caractère isolé trouvé dans <em>listecar</em></p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p>Tout caractère isolé non trouvé dans <em>listecar</em></p></td>
</tr>
</tbody>
</table>


Vous pouvez utiliser un groupe d’un ou plusieurs caractères *(liste* de caractères) placés entre crochets ( ) pour faire correspondre n’importe quel caractère dans l’expression, et la liste de caractères peut inclure presque tous les caractères du jeu de \[ \] caractères  ANSI,  y compris les chiffres. Vous pouvez utiliser les caractères spéciaux crochet ouvrant ( ), point d’interrogation (?), signe de nombre ( ) et astérisque ( ) pour se mettre en correspondance directement uniquement s’il est entre \[ \# \* crochets. Vous ne pouvez pas utiliser le crochet fermant () au sein d’un groupe pour correspondre à lui-même, mais vous pouvez l’utiliser en dehors d’un groupe \] comme caractère individuel.

Outre une simple liste de caractères encadrée par des crochets, *listecar* peut spécifier une plage de caractères en utilisant un tiret (-) pour séparer la borne supérieure et la borne inférieure de la plage. Par exemple, l’utilisation de A à Z dans le modèle entraîne une correspondance si la position du caractère correspondant dans l’expression contient l’une des lettres majuscules de la plage \[ \] A à Z.   Vous pouvez inclure plusieurs plages entre crochets sans les délimiter. Par exemple, \[ a-zA-Z0-9 correspond à \] n’importe quel caractère alphanumérique.

Il est important de noter que les caractères génériques ANSI SQL (%) et ( ) sont disponibles uniquement avec Microsoft Jet version 4.X et le fournisseur \_ Microsoft OLE DB pour Jet. Ils sont interprétés comme des caractères littéraux lors de l'utilisation avec Microsoft Access ou DAO.

Les autres règles importantes en matière de correspondance de chaîne sont les suivantes :

- Un point d’exclamation ( ) au début de la liste de caractères signifie qu’une correspondance est trouvée si un caractère, à l’exception de ceux de la liste de caractères, est trouvé \! dans  *l’expression*.  Utilisé hors des crochets, le point d'exclamation se recherche lui-même..

- Vous pouvez utiliser le tiret (-) au début (après un point d'exclamation s'il y en a un) ou à la fin de *listecar* pour qu'il se recherche lui-même. Placé à tout autre endroit, le tiret sert à identifier une plage de caractères ANSI

- Lorsque vous spécifiez une plage de caractères, ces derniers doivent apparaître en ordre ascendant (A-Z ou 0-100). \[A-Z \] est un modèle valide, mais ce \[ n’est pas le cas de \] Z-A.

- La séquence de caractères est ignorée ; elle est considérée comme une chaîne \[ \] nulle («  »).

