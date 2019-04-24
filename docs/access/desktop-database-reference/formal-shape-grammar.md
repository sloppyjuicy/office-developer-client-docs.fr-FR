---
title: Grammaire de forme formelle
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292320"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="1c61c-102">Grammaire de forme formelle</span><span class="sxs-lookup"><span data-stu-id="1c61c-102">Formal shape grammar</span></span>

<span data-ttu-id="1c61c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c61c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c61c-104">Ci-dessous figure la grammaire formelle que vous devez utiliser pour créer des commandes de mise en forme (Shape) :</span><span class="sxs-lookup"><span data-stu-id="1c61c-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="1c61c-105">Les termes grammaticaux obligatoires sont des chaînes de texte délimitées par des signes « inférieur à » et « supérieur à » (« \<\> »).</span><span class="sxs-lookup"><span data-stu-id="1c61c-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="1c61c-106">Les termes facultatifs sont délimités par des\[ \]crochets droits («»).</span><span class="sxs-lookup"><span data-stu-id="1c61c-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="1c61c-107">Les termes de remplacement sont indiqués par une barre verticale (« | »).</span><span class="sxs-lookup"><span data-stu-id="1c61c-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="1c61c-108">Les termes de remplacement répétitifs sont indiqués par les points de suspension (« ... »).</span><span class="sxs-lookup"><span data-stu-id="1c61c-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="1c61c-109">*Alpha* indique une chaîne de caractères alphabétiques.</span><span class="sxs-lookup"><span data-stu-id="1c61c-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="1c61c-110">*Digit* indique une chaîne numérique.</span><span class="sxs-lookup"><span data-stu-id="1c61c-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="1c61c-111">*Unicode-digit* indique une chaîne de chiffres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1c61c-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="1c61c-112">Tous les autres termes sont des littéraux.</span><span class="sxs-lookup"><span data-stu-id="1c61c-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c61c-113">Terme</span><span class="sxs-lookup"><span data-stu-id="1c61c-113">Term</span></span></p></th>
<th><p><span data-ttu-id="1c61c-114">Définition</span><span class="sxs-lookup"><span data-stu-id="1c61c-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-115">&lt;Shape-Command&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-116">Forme [&lt;table-exp&gt; [[As] &lt;alias&gt;]] [&lt;forme-action&gt;]</span><span class="sxs-lookup"><span data-stu-id="1c61c-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-118">{&lt;Provider-Command-Text&gt;} |</span><span class="sxs-lookup"><span data-stu-id="1c61c-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="1c61c-119">(&lt;forme-commande&gt;) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="1c61c-120">Nom &lt;de la table entre guillemets&gt; |</span><span class="sxs-lookup"><span data-stu-id="1c61c-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="1c61c-121">&lt;quoted-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-122">&lt;Shape-action&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-123">Ajouter &lt;un alias-liste de champs&gt; |</span><span class="sxs-lookup"><span data-stu-id="1c61c-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="1c61c-124">Compute &lt;alias-Field-List&gt; [by &lt;-liste&gt;de champs]</span><span class="sxs-lookup"><span data-stu-id="1c61c-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-125">&lt;alias-List-Field&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-126">&lt;alias-Field&gt; [, &lt;Aliased-Field... &gt;]</span><span class="sxs-lookup"><span data-stu-id="1c61c-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-127">&lt;alias-Field&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-128">&lt;Field-exp&gt; [[As] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="1c61c-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-129">&lt;champ-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-130">(&lt;relation-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-131">&lt;calculé-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="1c61c-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="1c61c-132">&lt;Aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="1c61c-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="1c61c-133">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-135">&lt;table-exp&gt; [[As] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="1c61c-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="1c61c-136">&lt;table-exp&gt; [[As] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="1c61c-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-137">&lt;relation-cond-List&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="1c61c-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-140">&lt;nom&gt; de champ à &lt;référence enfant&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-141">&lt;Référence enfant&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-142">&lt;nom de champ&gt; |</span><span class="sxs-lookup"><span data-stu-id="1c61c-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="1c61c-143">PARAMÈTRE &lt;param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-144">&lt;Param-Ref&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-145">&lt;valeur&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-146">&lt;liste de champs&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-147">&lt;nom&gt; de champ [, &lt;champ-nom&gt;]</span><span class="sxs-lookup"><span data-stu-id="1c61c-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-148">&lt;Aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-149">SUM (&lt;Qualified-Field-&gt;Name) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-150">AVG (&lt;Qualified-Field-&gt;Name) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-151">MIN (&lt;Qualified-Field-&gt;Name) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-152">MAX (&lt;nom&gt;de champ qualifié) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-153">Count (&lt;&gt; | &lt;nom&gt;qualifié d'alias complet) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-154">STDEV (&lt;Qualified-Field-&gt;Name) |</span><span class="sxs-lookup"><span data-stu-id="1c61c-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="1c61c-155">ANY (&lt;nom&gt;de champ qualifié)</span><span class="sxs-lookup"><span data-stu-id="1c61c-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-156">&lt;calculé-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-157">CALC (&lt;expression&gt;)</span><span class="sxs-lookup"><span data-stu-id="1c61c-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-158">&lt;nom de champ qualifié&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-159">&lt;alias&gt;. [&lt;alias&gt;...] &lt;nom de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-161">&lt;quoted-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-162">&lt;nom de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-163">&lt;quoted-&gt; name [[As &lt;]&gt;alias]</span><span class="sxs-lookup"><span data-stu-id="1c61c-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-164">&lt;quoted-Name&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-165">&quot;&lt;chaîne&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="1c61c-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="1c61c-166">'&lt;chaîne&gt;' |</span><span class="sxs-lookup"><span data-stu-id="1c61c-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="1c61c-167">[&lt;String&gt;] |</span><span class="sxs-lookup"><span data-stu-id="1c61c-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="1c61c-168">&lt;nom&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-169">&lt;nom qualifié&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-170">alias [. alias...]</span><span class="sxs-lookup"><span data-stu-id="1c61c-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-171">&lt;nom&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-172">alpha [alpha | chiffre | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="1c61c-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-173">&lt;valeur&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-174">chiffre [chiffre...]</span><span class="sxs-lookup"><span data-stu-id="1c61c-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-175">&lt;New-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-176">New &lt;Field-type&gt; [(&lt;nombre&gt; [, &lt;nombre&gt;])]</span><span class="sxs-lookup"><span data-stu-id="1c61c-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-177">&lt;type de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-178">Type de données OLE DB ou ADO.</span><span class="sxs-lookup"><span data-stu-id="1c61c-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c61c-179">&lt;chaîne&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-180">Unicode-Char [Unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="1c61c-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c61c-181">&lt;expression&gt;</span><span class="sxs-lookup"><span data-stu-id="1c61c-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="1c61c-182">Expression Visual Basic pour Applications dont les opérandes sont d'autres colonnes non calculées dans la même ligne.</span><span class="sxs-lookup"><span data-stu-id="1c61c-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

