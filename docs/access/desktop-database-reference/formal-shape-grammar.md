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
# <a name="formal-shape-grammar"></a><span data-ttu-id="7dab3-102">Grammaire de forme formelle</span><span class="sxs-lookup"><span data-stu-id="7dab3-102">Formal shape grammar</span></span>

<span data-ttu-id="7dab3-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dab3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dab3-104">Ci-dessous figure la grammaire formelle que vous devez utiliser pour créer des commandes de mise en forme (Shape) :</span><span class="sxs-lookup"><span data-stu-id="7dab3-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="7dab3-105">Les termes grammaticaux obligatoires sont des chaînes de texte délimitées par des signes « inférieur à » et « supérieur à » (« \<\> »).</span><span class="sxs-lookup"><span data-stu-id="7dab3-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="7dab3-106">Les termes facultatifs sont délimités par des crochets ( » \[ \] « ).</span><span class="sxs-lookup"><span data-stu-id="7dab3-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="7dab3-107">Les termes de remplacement sont indiqués par une barre verticale (« | »).</span><span class="sxs-lookup"><span data-stu-id="7dab3-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="7dab3-108">Les termes de remplacement répétitifs sont indiqués par les points de suspension (« ... »).</span><span class="sxs-lookup"><span data-stu-id="7dab3-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="7dab3-109">*Alpha* indique une chaîne de caractères alphabétiques.</span><span class="sxs-lookup"><span data-stu-id="7dab3-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="7dab3-110">*Digit* indique une chaîne numérique.</span><span class="sxs-lookup"><span data-stu-id="7dab3-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="7dab3-111">*Unicode-digit* indique une chaîne de chiffres Unicode.</span><span class="sxs-lookup"><span data-stu-id="7dab3-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="7dab3-112">Tous les autres termes sont des littéraux.</span><span class="sxs-lookup"><span data-stu-id="7dab3-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7dab3-113">Terme</span><span class="sxs-lookup"><span data-stu-id="7dab3-113">Term</span></span></p></th>
<th><p><span data-ttu-id="7dab3-114">Définition</span><span class="sxs-lookup"><span data-stu-id="7dab3-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-115">&lt;shape-command&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-116">SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-118">{ &lt; provider-command-text &gt; } |</span><span class="sxs-lookup"><span data-stu-id="7dab3-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="7dab3-119">( &lt; shape-command &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="7dab3-120">TABLE &lt; quoted-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="7dab3-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="7dab3-121">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-122">&lt;shape-action&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-123">APPEND &lt; aliased-field-list&gt; |</span><span class="sxs-lookup"><span data-stu-id="7dab3-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="7dab3-124">COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list] &gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-125">&lt;aliased-field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-126">&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-127">&lt;aliased-field&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-128">&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-129">&lt;field-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-130">( &lt; relation-exp &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-131">&lt;calculated-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="7dab3-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="7dab3-132">&lt;aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="7dab3-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="7dab3-133">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-135">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="7dab3-136">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-137">&lt;relation-cond-list&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-138">&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</span><span class="sxs-lookup"><span data-stu-id="7dab3-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-140">&lt;field-name &gt; TO &lt; child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-141">&lt;child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-142">&lt;field-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="7dab3-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="7dab3-143">PARAMETER &lt; param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-145">&lt;number&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-146">&lt;field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-147">&lt;field-name &gt; [, &lt; field-name &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-148">&lt;aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-149">SUM( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-150">AVG( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-151">MIN( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-152">MAX( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-153">COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-154">STDEV( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="7dab3-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="7dab3-155">ANY( &lt; qualified-field-name &gt; )</span><span class="sxs-lookup"><span data-stu-id="7dab3-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-156">&lt;calculated-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-157">CALC( &lt; expression &gt; )</span><span class="sxs-lookup"><span data-stu-id="7dab3-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-158">&lt;qualified-field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-159">&lt;alias &gt; .[ &lt; alias &gt; ...] &lt; field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-161">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-162">&lt;field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-163">&lt;quoted-name &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="7dab3-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-164">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-165">&quot;&lt;string&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="7dab3-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="7dab3-166">' &lt; string &gt; ' |</span><span class="sxs-lookup"><span data-stu-id="7dab3-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="7dab3-167">[ &lt; string &gt; ] |</span><span class="sxs-lookup"><span data-stu-id="7dab3-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="7dab3-168">&lt;name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-169">&lt;qualified-name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-170">alias[.alias...]</span><span class="sxs-lookup"><span data-stu-id="7dab3-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-171">&lt;name&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-172">alpha [ alpha | chiffre | _ | # | : | ...]</span><span class="sxs-lookup"><span data-stu-id="7dab3-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-173">&lt;number&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-174">chiffre [chiffre...]</span><span class="sxs-lookup"><span data-stu-id="7dab3-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-175">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-176">NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</span><span class="sxs-lookup"><span data-stu-id="7dab3-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-177">&lt;type de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-178">Type de données OLE DB ou ADO.</span><span class="sxs-lookup"><span data-stu-id="7dab3-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dab3-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-180">unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="7dab3-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dab3-181">&lt;expression&gt;</span><span class="sxs-lookup"><span data-stu-id="7dab3-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="7dab3-182">Expression Visual Basic pour Applications dont les opérandes sont d'autres colonnes non calculées dans la même ligne.</span><span class="sxs-lookup"><span data-stu-id="7dab3-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

