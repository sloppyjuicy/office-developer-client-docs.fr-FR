---
title: Fonctions d’agrégation, fonction CALC et mot-clé NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297192"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>Fonctions d’agrégation, fonction CALC et mot-clé NEW


**S’applique à** : Access 2013, Office 2013

La mise en forme des données prend en charge les fonctions suivantes. Le nom attribué au chapitre contenant la colonne à manipuler est *alias-chapitre*.

Un alias-chapitre peut être complètement qualifié et se composer de chaque nom de colonne de chapitre menant au chapitre contenant le *nom-colonne,*, le tout séparé par des points. Par exemple si le chapitre parent, chap1, contient un chapitre enfant, chap2, avec une colonne de montant, mnt, le nom qualifié sera chap1.chap2.mnt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fonctions d’agrégation</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SUM(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcule la somme de toutes les valeurs dans la colonne spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>AVG(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcule la moyenne de toutes les valeurs dans la colonne spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>MAX(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcule la valeur maximale dans la colonne spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>MIN(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcule la valeur minimale dans la colonne spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT(<em>chapter-alias</em>[.<em> column-name</em>])</p></td>
<td><p>Compte le nombre de lignes dans l'alias spécifié. Si une colonne est spécifiée, seules les lignes pour lesquelles cette colonne n'est pas Null, sont comptées.</p></td>
</tr>
<tr class="even">
<td><p>STDEV(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Calcule l'écart type dans la colonne spécifiée.</p></td>
</tr>
<tr class="odd">
<td><p>ANY(<em>chapter-alias</em>.<em> column-name</em>)</p></td>
<td><p>Valeur de la colonne spécifiée. ANY a une valeur prévisible uniquement si la valeur de la colonne est identique pour toutes les lignes du chapitre.</p><p><strong>REMARQUE</strong>: si la colonne ne contient pas la même valeur pour toutes les lignes du chapitre, la commande SHAPE renvoie arbitrairement l’une des valeurs comme valeur de la fonction ANY.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Expression calculée</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC(<em>expression</em>)</p></td>
<td><p>Calcule une expression arbitraire, mais uniquement sur la ligne de l’objet <strong>Recordset</strong> contenant la fonction CALC. Toute expression utilisant ces <a href="visual-basic-for-applications-functions.md"> fonctions Visual Basic pour Applications (VBA)</a> est autorisée.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Mot clé NEW</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NEW <em>field-type</em> [(<em>width</em>  |  <em>scale</em>  |  <em>precision</em>  |  <em>error</em> [, <em>scale</em>  |  <em>error</em>])]</p></td>
<td><p>Ajoute une colonne vide du type spécifié au <strong>recordset</strong>.</p></td>
</tr>
</tbody>
</table>

<br/>

Le *type de champ transmis* avec le mot clé NEW peut être l’un des types de données suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Types de données OLE DB</p></th>
<th><p>Type de données ADO équivalent(s)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>adBSTR</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adBoolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adUnsignedTinyInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adTinyInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adUnsignedSmallInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adUnsignedInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adBigInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adUnsignedBigInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adGuid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>adBinary, AdVarBinary, adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>adChar, adVarChar, adLongVarChar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>adWChar, adVarWChar, adLongVarWChar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>adDBDate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>adDBTime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>adDBTimeStamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adFileTime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>adError</p></td>
</tr>
</tbody>
</table>


Lorsque le nouveau champ est de type décimal (dans OLE DB, DBTYPE DECIMAL ou dans \_ ADO, adDecimal), vous devez spécifier les valeurs de précision et d’échelle.

