---
title: Grammaire de forme formelle
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 553eb116837cd760eecf630735070ecc13708287
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628788"
---
# <a name="formal-shape-grammar"></a>Grammaire de forme formelle

**S’applique à** : Access 2013, Office 2013

Ci-dessous figure la grammaire formelle que vous devez utiliser pour créer des commandes de mise en forme (Shape) :

  - Les termes grammaticaux obligatoires sont des chaînes de texte délimitées par des signes « inférieur à » et « supérieur à » (« \<\> »).

  - Les termes facultatifs sont délimités par des crochets ( »\[ \]« ).

  - Les termes de remplacement sont indiqués par une barre verticale (« | »).

  - Les termes de remplacement répétitifs sont indiqués par les points de suspension (« ... »).

  - *Alpha* indique une chaîne de caractères alphabétiques.

  - *Digit* indique une chaîne numérique.

  - *Unicode-digit* indique une chaîne de chiffres Unicode.

Tous les autres termes sont des littéraux.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Terme</p></th>
<th><p>Définition</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;shape-command&gt;</p></td>
<td><p>SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{&lt;provider-command-text&gt;} |<br />
(&lt;shape-command&gt;) |<br />
TABLE &lt;quoted-name&gt; |<br />
&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;shape-action&gt;</p></td>
<td><p>APPEND &lt;aliased-field-list&gt; |</p>
<p>COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aliased-field&gt;</p></td>
<td><p>&lt;field-exp&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-exp&gt;</p></td>
<td><p>(&lt;relation-exp&gt;) |</p>
<p>&lt;calculated-exp&gt; |</p>
<p>&lt;aggregate-exp&gt; |</p>
<p>&lt;new-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;table-exp&gt; [alias [AS]&gt;&lt;</p>
<p>&lt;table-exp&gt; [alias [AS]&gt;&lt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-list&gt;</p></td>
<td><p>&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;field-name&gt; TO &lt;child-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;child-ref&gt;</p></td>
<td><p>&lt;field-name&gt; |</p>
<p>PARAMETER &lt;param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;number&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-list&gt;</p></td>
<td><p>&lt;field-name&gt; [, &lt;field-name&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>SUM(&lt;qualified-field-name&gt;) |</p>
<p>AVG(&lt;qualified-field-name&gt;) |</p>
<p>Min(&lt;qualified-field-name&gt;) |</p>
<p>Max(&lt;qualified-field-name&gt;) |</p>
<p>Count(&lt;qualified-aliasqualified-name&gt;&gt; | &lt;) |</p>
<p>StDEV(&lt;qualified-field-name&gt;) |</p>
<p>ANY(&lt;qualified-field-name&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC(&lt;expression&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-field-name&gt;</p></td>
<td><p>&lt;alias&gt;.[&lt; alias&gt;...]&lt; field-name&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;alias&gt;</p></td>
<td><p>&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;field-name&gt;</p></td>
<td><p>&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;quoted-name&gt;</p></td>
<td><p>&quot;&lt;string&gt;&quot; |</p>
<p>'&lt;string&gt;' |</p>
<p>[&lt;string&gt;] |</p>
<p>&lt;nom&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-name&gt;</p></td>
<td><p>alias[.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;nom&gt;</p></td>
<td><p>alpha [ alpha | chiffre | _ | # | : | ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;number&gt;</p></td>
<td><p>chiffre [chiffre...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;type de champ&gt;</p></td>
<td><p>Type de données OLE DB ou ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Expression Visual Basic pour Applications dont les opérandes sont d'autres colonnes non calculées dans la même ligne.</p></td>
</tr>
</tbody>
</table>

