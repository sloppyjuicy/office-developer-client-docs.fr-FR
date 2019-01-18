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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716900"
---
# <a name="using-wildcard-characters-in-string-comparisons"></a><span data-ttu-id="d3cfb-102">Utilisation de caractères génériques dans les comparaisons de chaînes</span><span class="sxs-lookup"><span data-stu-id="d3cfb-102">Using wildcard characters in string comparisons</span></span>

<span data-ttu-id="d3cfb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3cfb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3cfb-p101">La fonction intégrée de recherche des correspondances de chaînes constitue un outil polyvalent permettant de comparer des chaînes. Le tableau suivant montre les caractères génériques que vous pouvez utiliser avec l'opérateur **Like** ainsi que les chiffres ou les chaînes auxquels ils correspondent.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-p101">Built-in pattern matching provides a versatile tool for making string comparisons. The following table shows the wildcard characters you can use with the **Like** operator and the number of digits or strings they match.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d3cfb-106">Caractère (s) dans <em>motif</em></span><span class="sxs-lookup"><span data-stu-id="d3cfb-106">Character(s) in <em>pattern</em></span></span></p></th>
<th><p><span data-ttu-id="d3cfb-107">Correspondances dans <em>expression</em></span><span class="sxs-lookup"><span data-stu-id="d3cfb-107">Matches in <em>expression</em></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d3cfb-p102">? ou _ (caractère de soulignement)</span><span class="sxs-lookup"><span data-stu-id="d3cfb-p102">? or _ (underscore)</span></span></p></td>
<td><p><span data-ttu-id="d3cfb-110">Tout caractère isolé</span><span class="sxs-lookup"><span data-stu-id="d3cfb-110">Any single character</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3cfb-111">\*ou %</span><span class="sxs-lookup"><span data-stu-id="d3cfb-111">\* or %</span></span></p></td>
<td><p><span data-ttu-id="d3cfb-112">Zéro, un ou plusieurs caractères</span><span class="sxs-lookup"><span data-stu-id="d3cfb-112">Zero or more characters</span></span></p></td>
</tr>
<tr class="odd">
<td><p>#</p></td>
<td><p><span data-ttu-id="d3cfb-113">Tout chiffre isolé (0 à 9)</span><span class="sxs-lookup"><span data-stu-id="d3cfb-113">Any single digit (0 – 9)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d3cfb-114">[<em>listecar</em>]</span><span class="sxs-lookup"><span data-stu-id="d3cfb-114">[<em>charlist</em>]</span></span></p></td>
<td><p><span data-ttu-id="d3cfb-115">Tout caractère unique dans <em>charlist</em></span><span class="sxs-lookup"><span data-stu-id="d3cfb-115">Any single character in <em>charlist</em></span></span></p></td>
</tr>
<tr class="odd">
<td><p>[!<em>listecar</em>]</p></td>
<td><p><span data-ttu-id="d3cfb-117">Tout caractère unique non trouvé dans <em>listecar</em></span><span class="sxs-lookup"><span data-stu-id="d3cfb-117">Any single character not in <em>charlist</em></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d3cfb-118">Vous pouvez utiliser un groupe d’un ou plusieurs caractères (*argument charlist*) placés entre crochets (\[ \]) pour faire correspondre tout caractère unique dans *expression,* sachant que *listecar* peut inclure tous les caractères dans le caractère ANSI défini, y compris chiffres.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-118">You can use a group of one or more characters (*charlist*) enclosed in brackets (\[ \]) to match any single character in *expression,* and *charlist* can include almost any characters in the ANSI character set, including digits.</span></span> <span data-ttu-id="d3cfb-119">Vous pouvez utiliser les caractères spéciaux crochet ouvrant (\[ ), point d’interrogation (?), le signe dièse (\#) et l’astérisque (\*) pour faire référence à eux-mêmes uniquement si entre crochets.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-119">You can use the special characters opening bracket (\[ ), question mark (?), number sign (\#), and asterisk (\*) to match themselves directly only if enclosed in brackets.</span></span> <span data-ttu-id="d3cfb-120">Vous ne pouvez pas utiliser le crochet fermant ( \]) au sein d’un groupe pour correspondre à lui-même, mais vous pouvez l’utiliser en dehors d’un groupe de caractères.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-120">You cannot use the closing bracket ( \]) within a group to match itself, but you can use it outside a group as an individual character.</span></span>

<span data-ttu-id="d3cfb-121">Outre une simple liste de caractères placés entourés crochets, *charlist* peut spécifier une plage de caractères à l’aide d’un trait d’union (-) pour séparer les deux et les limites inférieures de la plage.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-121">In addition to a simple list of characters enclosed in brackets, *charlist* can specify a range of characters by using a hyphen (-) to separate the upper and lower bounds of the range.</span></span> <span data-ttu-id="d3cfb-122">Par exemple, à l’aide de \[A-Z\] dans *pattern, une correspondance si la position du caractère correspondant dans *expression* contient une lettre majuscule dans la plage de A à Z* . Vous pouvez inclure plusieurs plages entre les crochets sans les délimiter.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-122">For example, using \[A-Z\] in *pattern* results in a match if the corresponding character position in *expression* contains any of the uppercase letters in the range A through Z. You can include multiple ranges within the brackets without delimiting the ranges.</span></span> <span data-ttu-id="d3cfb-123">Par exemple, \[a-zA-Z0-9\] correspond à n’importe quel caractère alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-123">For example, \[a-zA-Z0-9\] matches any alphanumeric character.</span></span>

<span data-ttu-id="d3cfb-124">Il est important de noter que les caractères génériques SQL ANSI (%) et (\_) sont uniquement disponibles avec Microsoft Jet version 4.X et le fournisseur Microsoft OLE DB pour Jet.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-124">It is important to note that the ANSI SQL wildcards (%) and (\_) are only available with Microsoft Jet version 4.X and the Microsoft OLE DB Provider for Jet.</span></span> <span data-ttu-id="d3cfb-125">Ils sont interprétés comme des caractères littéraux lors de l'utilisation avec Microsoft Access ou DAO.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-125">They will be treated as literals if used through Microsoft Access or DAO.</span></span>

<span data-ttu-id="d3cfb-126">Les autres règles importantes en matière de correspondance de chaîne sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3cfb-126">Other important rules for pattern matching include the following:</span></span>

- <span data-ttu-id="d3cfb-127">Un point d’exclamation (\!) au début de *charlist* signifie que la correspondance est établie si tout caractère sauf ceux présents dans *listecar* sont trouve dans *expression*.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-127">An exclamation mark (\!) at the beginning of *charlist* means that a match is made if any character except those in *charlist* are found in *expression*.</span></span> <span data-ttu-id="d3cfb-128">Utilisé hors des crochets, le point d'exclamation se recherche lui-même..</span><span class="sxs-lookup"><span data-stu-id="d3cfb-128">When used outside brackets, the exclamation mark matches itself.</span></span>

- <span data-ttu-id="d3cfb-129">Vous pouvez utiliser le trait d’union (-) au début (après un point d’exclamation si elle est utilisée) ou à la fin de *l’argument charlist* pour correspondre à lui-même.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-129">You can use the hyphen (-) either at the beginning (after an exclamation mark if one is used) or at the end of *charlist* to match itself.</span></span> <span data-ttu-id="d3cfb-130">Placé à tout autre endroit, le tiret sert à identifier une plage de caractères ANSI</span><span class="sxs-lookup"><span data-stu-id="d3cfb-130">In any other location, the hyphen identifies a range of ANSI characters.</span></span>

- <span data-ttu-id="d3cfb-131">Lorsque vous spécifiez une plage de caractères, ces derniers doivent apparaître en ordre ascendant (A-Z ou 0-100).</span><span class="sxs-lookup"><span data-stu-id="d3cfb-131">When you specify a range of characters, the characters must appear in ascending sort order (A-Z or 0-100).</span></span> <span data-ttu-id="d3cfb-132">\[A-Z\] est un modèle valide, mais \[Z-A\] n’est pas.</span><span class="sxs-lookup"><span data-stu-id="d3cfb-132">\[A-Z\] is a valid pattern, but \[Z-A\] is not.</span></span>

- <span data-ttu-id="d3cfb-133">La séquence de caractères \[ \] est ignorée ; elle est considérée comme une chaîne de longueur nulle ( » »).</span><span class="sxs-lookup"><span data-stu-id="d3cfb-133">The character sequence \[ \] is ignored; it is considered to be a zero-length string ("").</span></span>

