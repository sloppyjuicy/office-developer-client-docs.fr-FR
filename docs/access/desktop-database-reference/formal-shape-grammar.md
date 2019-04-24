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
# <a name="formal-shape-grammar"></a>Grammaire de forme formelle

**S’applique à** : Access 2013, Office 2013

Ci-dessous figure la grammaire formelle que vous devez utiliser pour créer des commandes de mise en forme (Shape) :

  - Les termes grammaticaux obligatoires sont des chaînes de texte délimitées par des signes « inférieur à » et « supérieur à » (« \<\> »).

  - Les termes facultatifs sont délimités par des\[ \]crochets droits («»).

  - Les termes de remplacement sont indiqués par une barre verticale (« | »).

  - Les termes de remplacement répétitifs sont indiqués par les points de suspension (« ... »).

  - *Alpha* indique une chaîne de caractères alphabétiques.

  - *Digit* indique une chaîne numérique.

  - *Unicode-digit* indique une chaîne de chiffres Unicode.

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
<td><p>&lt;Shape-Command&gt;</p></td>
<td><p>Forme [&lt;table-exp&gt; [[As] &lt;alias&gt;]] [&lt;forme-action&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{&lt;Provider-Command-Text&gt;} |<br />
(&lt;forme-commande&gt;) |<br />
Nom &lt;de la table entre guillemets&gt; |<br />
&lt;quoted-Name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Shape-action&gt;</p></td>
<td><p>Ajouter &lt;un alias-liste de champs&gt; |</p>
<p>Compute &lt;alias-Field-List&gt; [by &lt;-liste&gt;de champs]</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias-List-Field&gt;</p></td>
<td><p>&lt;alias-Field&gt; [, &lt;Aliased-Field... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;alias-Field&gt;</p></td>
<td><p>&lt;Field-exp&gt; [[As] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;champ-exp&gt;</p></td>
<td><p>(&lt;relation-exp&gt;) |</p>
<p>&lt;calculé-exp&gt; |</p>
<p>&lt;Aggregate-exp&gt; |</p>
<p>&lt;New-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp&gt; [[As] &lt;alias&gt;]</p>
<p>&lt;table-exp&gt; [[As] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-List&gt;</p></td>
<td><p>&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;nom&gt; de champ à &lt;référence enfant&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Référence enfant&gt;</p></td>
<td><p>&lt;nom de champ&gt; |</p>
<p>PARAMÈTRE &lt;param-Ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Param-Ref&gt;</p></td>
<td><p>&lt;valeur&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;liste de champs&gt;</p></td>
<td><p>&lt;nom&gt; de champ [, &lt;champ-nom&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aggregate-exp&gt;</p></td>
<td><p>SUM (&lt;Qualified-Field-&gt;Name) |</p>
<p>AVG (&lt;Qualified-Field-&gt;Name) |</p>
<p>MIN (&lt;Qualified-Field-&gt;Name) |</p>
<p>MAX (&lt;nom&gt;de champ qualifié) |</p>
<p>Count (&lt;&gt; | &lt;nom&gt;qualifié d'alias complet) |</p>
<p>STDEV (&lt;Qualified-Field-&gt;Name) |</p>
<p>ANY (&lt;nom&gt;de champ qualifié)</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculé-exp&gt;</p></td>
<td><p>CALC (&lt;expression&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nom de champ qualifié&gt;</p></td>
<td><p>&lt;alias&gt;. [&lt;alias&gt;...] &lt;nom de champ&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;quoted-Name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nom de champ&gt;</p></td>
<td><p>&lt;quoted-&gt; name [[As &lt;]&gt;alias]</p></td>
</tr>
<tr class="even">
<td><p>&lt;quoted-Name&gt;</p></td>
<td><p>&quot;&lt;chaîne&gt;&quot; |</p>
<p>'&lt;chaîne&gt;' |</p>
<p>[&lt;String&gt;] |</p>
<p>&lt;nom&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;nom qualifié&gt;</p></td>
<td><p>alias [. alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nom&gt;</p></td>
<td><p>alpha [alpha | chiffre | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;valeur&gt;</p></td>
<td><p>chiffre [chiffre...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;New-exp&gt;</p></td>
<td><p>New &lt;Field-type&gt; [(&lt;nombre&gt; [, &lt;nombre&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;type de champ&gt;</p></td>
<td><p>Type de données OLE DB ou ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;chaîne&gt;</p></td>
<td><p>Unicode-Char [Unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Expression Visual Basic pour Applications dont les opérandes sont d'autres colonnes non calculées dans la même ligne.</p></td>
</tr>
</tbody>
</table>

