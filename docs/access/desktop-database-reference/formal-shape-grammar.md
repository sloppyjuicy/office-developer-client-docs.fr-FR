---
title: Grammaire de mise en forme formelle
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06548b96a3c23014f23b5123965476c5d1149b6d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472160"
---
# <a name="formal-shape-grammar"></a>Grammaire de mise en forme formelle


**S’applique à**: Access 2013 | Office 2013

Ci-dessous figure la grammaire formelle que vous devez utiliser pour créer des commandes de mise en forme (Shape) :

  - Les termes grammaticaux obligatoires sont des chaînes de texte délimitées par des signes « inférieur à » et « supérieur à » (« \<\> »).

  - Les termes facultatifs sont délimités par des crochets droits («\[ \]»).

  - Les termes de remplacement sont indiqués par une barre verticale (« | »).

  - Les termes de remplacement répétitifs sont indiqués par les points de suspension (« ... »).

  - *Alpha* indique une chaîne de caractères alphabétiques.

  - *Digit* indique une chaîne de nombres.

  - *Unicode-digit* indique une chaîne de chiffres unicode.

Tous les autres termes sont des littéraux.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Terme</p></th>
<th><p>Définition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;commande de la forme&gt;</p></td>
<td><p>FORME [&lt;table-exp&gt; [[AS] &lt;alias&gt;]] [&lt;-action de la forme&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;tableau-exp&gt;</p></td>
<td><p>{&lt;texte de commande fournisseur&gt;} |<br />
(&lt;-commande shape&gt;) |<br />
TABLE &lt;nom entre guillemets&gt; |<br />
&lt;nom entre guillemets&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;action de la forme&gt;</p></td>
<td><p>APPEND &lt;alias liste de champs&gt; |</p>
<p>CALCULER &lt;liste de champs alias&gt; [BY &lt;-liste de champs&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;liste de champs d’alias&gt;</p></td>
<td><p>&lt;champ alias&gt; [, &lt;champ alias... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;champ de l’alias&gt;</p></td>
<td><p>&lt;champ-exp&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;champ-exp&gt;</p></td>
<td><p>(&lt;relation-exp&gt;) |</p>
<p>&lt;exp calculée&gt; |</p>
<p>&lt;agrégat-exp&gt; |</p>
<p>&lt;nouvelle exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;tableau-exp&gt; [[AS] &lt;alias&gt;]</p>
<p>&lt;tableau-exp&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;liste de condition de relation&gt;</p></td>
<td><p>&lt;condition de la relation&gt; [, &lt;soumis à la relation&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;condition de la relation&gt;</p></td>
<td><p>&lt;nom du champ&gt; à &lt;-ref enfants&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;référence de l’enfant&gt;</p></td>
<td><p>&lt;nom de champ&gt; |</p>
<p>PARAMÈTRE &lt;param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Param-ref&gt;</p></td>
<td><p>&lt;nombre&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;liste des champs&gt;</p></td>
<td><p>&lt;nom du champ&gt; [, &lt;-nom de champ&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;agrégat-exp&gt;</p></td>
<td><p>Somme (&lt;nom de champ qualifié&gt;) |</p>
<p>AVG (&lt;nom de champ qualifié&gt;) |</p>
<p>MIN (&lt;nom de champ qualifié&gt;) |</p>
<p>MAX (&lt;nom de champ qualifié&gt;) |</p>
<p>COUNT (&lt;alias qualifié&gt; | &lt;nom qualifié&gt;) |</p>
<p>STDEV (&lt;nom de champ qualifié&gt;) |</p>
<p>TOUT (&lt;nom de champ qualifié&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;exp calculée&gt;</p></td>
<td><p>CALC(&lt;expression&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nom de champ complet&gt;</p></td>
<td><p>&lt;alias&gt;. [&lt;alias&gt;...] &lt;-nom de champ&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;nom entre guillemets&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nom de champ&gt;</p></td>
<td><p>&lt;nom entre guillemets&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nom entre guillemets&gt;</p></td>
<td><p>&quot;&lt;chaîne&gt;&quot; |</p>
<p>«&lt;chaîne&gt;' |</p>
<p>[&lt;chaîne&gt;] |</p>
<p>&lt;nom&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nom complet&gt;</p></td>
<td><p>alias [.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nom&gt;</p></td>
<td><p>alpha [alpha | chiffre | _ | # | : |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nombre&gt;</p></td>
<td><p>chiffre [chiffre...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nouvelle exp&gt;</p></td>
<td><p>NOUVELLE &lt;type-champ&gt; [(&lt;numéro&gt; [, &lt;numéro&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;type de champ&gt;</p></td>
<td><p>Type de données OLE DB ou ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;chaîne&gt;</p></td>
<td><p>caractères Unicode [caractères unicode...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Expression Visual Basic pour Applications dont les opérandes sont d'autres colonnes non calculées dans la même ligne.</p></td>
</tr>
</tbody>
</table>

