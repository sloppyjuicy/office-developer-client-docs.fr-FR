---
title: Grammaire de mise en forme formelle
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de4f2eca0b5dd607cb9d93cc7e90f4af0ba8d89
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945536"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="60d18-102">Grammaire de mise en forme formelle</span><span class="sxs-lookup"><span data-stu-id="60d18-102">Formal shape grammar</span></span>

<span data-ttu-id="60d18-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60d18-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60d18-104">Ci-dessous figure la grammaire formelle que vous devez utiliser pour créer des commandes de mise en forme (Shape) :</span><span class="sxs-lookup"><span data-stu-id="60d18-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="60d18-105">Les termes grammaticaux obligatoires sont des chaînes de texte délimitées par des signes « inférieur à » et « supérieur à » (« \<\> »).</span><span class="sxs-lookup"><span data-stu-id="60d18-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="60d18-106">Les termes facultatifs sont délimités par des crochets droits («\[ \]»).</span><span class="sxs-lookup"><span data-stu-id="60d18-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="60d18-107">Les termes de remplacement sont indiqués par une barre verticale (« | »).</span><span class="sxs-lookup"><span data-stu-id="60d18-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="60d18-108">Les termes de remplacement répétitifs sont indiqués par les points de suspension (« ... »).</span><span class="sxs-lookup"><span data-stu-id="60d18-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="60d18-109">*Alpha* indique une chaîne de caractères alphabétiques.</span><span class="sxs-lookup"><span data-stu-id="60d18-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="60d18-110">*Digit* indique une chaîne de nombres.</span><span class="sxs-lookup"><span data-stu-id="60d18-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="60d18-111">*Unicode-digit* indique une chaîne de chiffres unicode.</span><span class="sxs-lookup"><span data-stu-id="60d18-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="60d18-112">Tous les autres termes sont des littéraux.</span><span class="sxs-lookup"><span data-stu-id="60d18-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60d18-113">Terme</span><span class="sxs-lookup"><span data-stu-id="60d18-113">Term</span></span></p></th>
<th><p><span data-ttu-id="60d18-114">Définition</span><span class="sxs-lookup"><span data-stu-id="60d18-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60d18-115">&lt;commande de la forme&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-116">FORME [&lt;table-exp&gt; [[AS] &lt;alias&gt;]] [&lt;-action de la forme&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-117">&lt;tableau-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-118">{&lt;texte de commande fournisseur&gt;} |</span><span class="sxs-lookup"><span data-stu-id="60d18-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="60d18-119">(&lt;-commande shape&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="60d18-120">TABLE &lt;nom entre guillemets&gt; |</span><span class="sxs-lookup"><span data-stu-id="60d18-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="60d18-121">&lt;nom entre guillemets&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-122">&lt;action de la forme&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-123">APPEND &lt;alias liste de champs&gt; |</span><span class="sxs-lookup"><span data-stu-id="60d18-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="60d18-124">CALCULER &lt;liste de champs alias&gt; [BY &lt;-liste de champs&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-125">&lt;liste de champs d’alias&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-126">&lt;champ alias&gt; [, &lt;champ alias... &gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-127">&lt;champ de l’alias&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-128">&lt;champ-exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-129">&lt;champ-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-130">(&lt;relation-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-131">&lt;exp calculée&gt; |</span><span class="sxs-lookup"><span data-stu-id="60d18-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="60d18-132">&lt;agrégat-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="60d18-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="60d18-133">&lt;nouvelle exp&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-135">&lt;tableau-exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="60d18-136">&lt;tableau-exp&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-137">&lt;liste de condition de relation&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-138">&lt;condition de la relation&gt; [, &lt;soumis à la relation&gt;...]</span><span class="sxs-lookup"><span data-stu-id="60d18-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-139">&lt;condition de la relation&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-140">&lt;nom du champ&gt; à &lt;-ref enfants&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-141">&lt;référence de l’enfant&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-142">&lt;nom de champ&gt; |</span><span class="sxs-lookup"><span data-stu-id="60d18-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="60d18-143">PARAMÈTRE &lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-144">&lt;Param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-145">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-146">&lt;liste des champs&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-147">&lt;nom du champ&gt; [, &lt;-nom de champ&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-148">&lt;agrégat-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-149">Somme (&lt;nom de champ qualifié&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-150">AVG (&lt;nom de champ qualifié&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-151">MIN (&lt;nom de champ qualifié&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-152">MAX (&lt;nom de champ qualifié&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-153">COUNT (&lt;alias qualifié&gt; | &lt;nom qualifié&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-154">STDEV (&lt;nom de champ qualifié&gt;) |</span><span class="sxs-lookup"><span data-stu-id="60d18-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="60d18-155">TOUT (&lt;nom de champ qualifié&gt;)</span><span class="sxs-lookup"><span data-stu-id="60d18-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-156">&lt;exp calculée&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-157">CALC(&lt;expression&gt;)</span><span class="sxs-lookup"><span data-stu-id="60d18-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-158">&lt;nom de champ complet&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-159">&lt;alias&gt;. [&lt;alias&gt;...] &lt;-nom de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-160">&lt;alias&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-161">&lt;nom entre guillemets&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-162">&lt;nom de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-163">&lt;nom entre guillemets&gt; [[AS] &lt;alias&gt;]</span><span class="sxs-lookup"><span data-stu-id="60d18-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-164">&lt;nom entre guillemets&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-165">&quot;&lt;chaîne&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="60d18-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="60d18-166">«&lt;chaîne&gt;' |</span><span class="sxs-lookup"><span data-stu-id="60d18-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="60d18-167">[&lt;chaîne&gt;] |</span><span class="sxs-lookup"><span data-stu-id="60d18-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="60d18-168">&lt;nom&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-169">&lt;nom complet&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-170">alias [.alias...]</span><span class="sxs-lookup"><span data-stu-id="60d18-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-171">&lt;nom&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-172">alpha [alpha | chiffre | _ | # | : |...]</span><span class="sxs-lookup"><span data-stu-id="60d18-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-173">&lt;nombre&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-174">chiffre [chiffre...]</span><span class="sxs-lookup"><span data-stu-id="60d18-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-175">&lt;nouvelle exp&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-176">NOUVELLE &lt;type-champ&gt; [(&lt;numéro&gt; [, &lt;numéro&gt;])]</span><span class="sxs-lookup"><span data-stu-id="60d18-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-177">&lt;type de champ&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-178">Type de données OLE DB ou ADO.</span><span class="sxs-lookup"><span data-stu-id="60d18-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60d18-179">&lt;chaîne&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-180">caractères Unicode [caractères unicode...]</span><span class="sxs-lookup"><span data-stu-id="60d18-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60d18-181">&lt;expression&gt;</span><span class="sxs-lookup"><span data-stu-id="60d18-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="60d18-182">Expression Visual Basic pour Applications dont les opérandes sont d'autres colonnes non calculées dans la même ligne.</span><span class="sxs-lookup"><span data-stu-id="60d18-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

