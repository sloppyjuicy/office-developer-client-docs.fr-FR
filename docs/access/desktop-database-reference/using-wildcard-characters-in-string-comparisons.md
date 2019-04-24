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
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="2fd37-102">Utilisation de caractères génériques dans les comparaisons de chaînes</span><span class="sxs-lookup"><span data-stu-id="2fd37-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="2fd37-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fd37-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fd37-p101">La fonction intégrée de recherche des correspondances de chaînes constitue un outil polyvalent permettant de comparer des chaînes. Le tableau suivant montre les caractères génériques que vous pouvez utiliser avec l'opérateur **Like** ainsi que les chiffres ou les chaînes auxquels ils correspondent.</span><span class="sxs-lookup"><span data-stu-id="2fd37-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2fd37-106">Caractère(s) dans <em>motif</em></span><span class="sxs-lookup"><span data-stu-id="2fd37-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="2fd37-107">Correspondances dans <em>expression</em></span><span class="sxs-lookup"><span data-stu-id="2fd37-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2fd37-p102">? ou _ (caractère de soulignement)</span><span class="sxs-lookup"><span data-stu-id="2fd37-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="2fd37-110">Un seul caractère</span><span class="sxs-lookup"><span data-stu-id="2fd37-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fd37-111">\*des</span><span class="sxs-lookup"><span data-stu-id="2fd37-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="2fd37-112">Zéro, un ou plusieurs caractères</span><span class="sxs-lookup"><span data-stu-id="2fd37-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="2fd37-113">Tout chiffre isolé (0 à 9)</span><span class="sxs-lookup"><span data-stu-id="2fd37-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2fd37-114">[<em>charlist</em>]</span><span class="sxs-lookup"><span data-stu-id="2fd37-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="2fd37-115">Tout caractère isolé trouvé dans <em>listecar</em></span><span class="sxs-lookup"><span data-stu-id="2fd37-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[! <em>charlist</em>]</p></td>
<td><p><span data-ttu-id="2fd37-117">Tout caractère isolé non trouvé dans <em>listecar</em></span><span class="sxs-lookup"><span data-stu-id="2fd37-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2fd37-118">Vous pouvez utiliser un groupe d'un ou de plusieurs caractères (*listecar*) placés entre crochets\[ \]() pour faire correspondre tout caractère unique dans *expression,* et *listecar* peut inclure tous les caractères du jeu de caractères ANSI, y compris numérique.</span><span class="sxs-lookup"><span data-stu-id="2fd37-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="2fd37-119">Vous pouvez utiliser le crochet ouvrant (\[ ), le point d'interrogation (?), le signe\#dièse () et l'\*astérisque () pour qu'ils correspondent directement uniquement s'ils sont entourés de crochets.</span><span class="sxs-lookup"><span data-stu-id="2fd37-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="2fd37-120">Vous ne pouvez pas utiliser le crochet \]fermant () au sein d'un groupe pour qu'il corresponde à lui-même, mais vous pouvez l'utiliser en dehors d'un groupe en tant que caractère individuel.</span><span class="sxs-lookup"><span data-stu-id="2fd37-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="2fd37-121">Outre une simple liste de caractères encadrée par des crochets, *listecar* peut spécifier une plage de caractères en utilisant un tiret (-) pour séparer la borne supérieure et la borne inférieure de la plage.</span><span class="sxs-lookup"><span data-stu-id="2fd37-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="2fd37-122">Par exemple, l' \[utilisation de A\] -Z dans *pattern* se traduit par une correspondance si la position du caractère correspondante dans *expression* contient l'une des lettres majuscules comprises entre A et Z. Vous pouvez inclure plusieurs plages entre les crochets sans délimiter les plages.</span><span class="sxs-lookup"><span data-stu-id="2fd37-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="2fd37-123">Par exemple, \[a-zA-z0-9\] correspond à n'importe quel caractère alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="2fd37-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="2fd37-124">Il est important de noter que les caractères génériques ANSI SQL (%) et (\_) sont disponibles uniquement avec Microsoft Jet version 4. X et le fournisseur Microsoft OLE DB pour jet.</span><span class="sxs-lookup"><span data-stu-id="2fd37-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="2fd37-125">Ils sont interprétés comme des caractères littéraux lors de l'utilisation avec Microsoft Access ou DAO.</span><span class="sxs-lookup"><span data-stu-id="2fd37-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="2fd37-126">Les autres règles importantes en matière de correspondance de chaîne sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2fd37-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="2fd37-127">Un point d'exclamation\!() au début de *listecar* signifie qu'une correspondance est trouvée si un caractère quelconque, sauf ceux de *charlist* , se trouve dans *expression*.</span><span class="sxs-lookup"><span data-stu-id="2fd37-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="2fd37-128">Utilisé hors des crochets, le point d'exclamation se recherche lui-même..</span><span class="sxs-lookup"><span data-stu-id="2fd37-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="2fd37-p107">Vous pouvez utiliser le tiret (-) au début (après un point d'exclamation s'il y en a un) ou à la fin de *listecar* pour qu'il se recherche lui-même. Placé à tout autre endroit, le tiret sert à identifier une plage de caractères ANSI</span><span class="sxs-lookup"><span data-stu-id="2fd37-p107">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself. In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="2fd37-131">Lorsque vous spécifiez une plage de caractères, ces derniers doivent apparaître en ordre ascendant (A-Z ou 0-100).</span><span class="sxs-lookup"><span data-stu-id="2fd37-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="2fd37-132">\[A-Z\] est un modèle valide, mais \[Z-a\] ne l'est pas.</span><span class="sxs-lookup"><span data-stu-id="2fd37-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="2fd37-133">La séquence \[ \] de caractères est ignorée; elle est considérée comme une chaîne de longueur nulle ("").</span><span class="sxs-lookup"><span data-stu-id="2fd37-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

