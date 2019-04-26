---
title: Types de données équivalents ANSI SQL
TOCTitle: Equivalent ANSI SQL data types
ms:assetid: 720abf59-f9ef-4e14-4223-c873f604ad58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195814(v=office.15)
ms:contentKeyID: 48545599
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277587
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 3ea0641c7325bfcb4339572bc8b50724115af8d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293510"
---
# <a name="equivalent-ansi-sql-data-types"></a>Types de données équivalents ANSI SQL


**S’applique à** : Access 2013, Office 2013

Le tableau suivant énumère les types de données ANSI SQL, les types de données SQL équivalents du moteur de base de données Microsoft Access et leurs synonymes valides. Il répertorie également les types de données Microsoft SQL Server™ équivalents.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Type de données ANSI SQL</p></th>
<th><p>Type de données Microsoft Access SQL</p></th>
<th><p>Synonyme</p></th>
<th><p>Type de données Microsoft SQL Server</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BIT, BIT VARYING</p></td>
<td><p>BINARY (voir Remarques)</p></td>
<td><p>VARBINARY, BINARY VARYING BIT VARYING</p></td>
<td><p>BINARY, VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>Non pris en charge</p></td>
<td><p>BIT (voir Remarques)</p></td>
<td><p>BOOLEAN, LOGICAL, LOGICAL1, YESNO</p></td>
<td><p>BIT</p></td>
</tr>
<tr class="odd">
<td><p>Non pris en charge</p></td>
<td><p>TINYINT</p></td>
<td><p>INTEGER1, BYTE</p></td>
<td><p>TINYINT</p></td>
</tr>
<tr class="even">
<td><p>Non pris en charge</p></td>
<td><p>COUNTER (voir Remarques)</p></td>
<td><p>AUTOINCREMENT</p></td>
<td><p>(voir Remarques)</p></td>
</tr>
<tr class="odd">
<td><p>Non pris en charge</p></td>
<td><p>MONEY</p></td>
<td><p>CURRENCY</p></td>
<td><p>MONEY</p></td>
</tr>
<tr class="even">
<td><p>DATE, TIME, TIMESTAMP</p></td>
<td><p>DATETIME</p></td>
<td><p>DATE, TIME (voir Remarques)</p></td>
<td><p>DATETIME</p></td>
</tr>
<tr class="odd">
<td><p>Non pris en charge</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
<td><p>GUID</p></td>
<td><p>UNIQUEIDENTIFIER</p></td>
</tr>
<tr class="even">
<td><p>DECIMAL</p></td>
<td><p>DECIMAL</p></td>
<td><p>NUMERIC, DEC</p></td>
<td><p>DECIMAL</p></td>
</tr>
<tr class="odd">
<td><p>REAL</p></td>
<td><p>REAL</p></td>
<td><p>SINGLE, FLOAT4, IEEESINGLE</p></td>
<td><p>REAL</p></td>
</tr>
<tr class="even">
<td><p>DOUBLE PRECISION, FLOAT</p></td>
<td><p>FLOAT</p></td>
<td><p>DOUBLE, FLOAT8, IEEEDOUBLE, NUMBER (voir Remarques)</p></td>
<td><p>FLOAT</p></td>
</tr>
<tr class="odd">
<td><p>SMALLINT</p></td>
<td><p>SMALLINT</p></td>
<td><p>SHORT, INTEGER2</p></td>
<td><p>SMALLINT</p></td>
</tr>
<tr class="even">
<td><p>INTEGER</p></td>
<td><p>INTEGER</p></td>
<td><p>LONG, INT, INTEGER4</p></td>
<td><p>INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>INTERVAL</p></td>
<td><p>Non pris en charge</p></td>
<td><p></p></td>
<td><p>Non prise en charge</p></td>
</tr>
<tr class="even">
<td><p>Non pris en charge</p></td>
<td><p>IMAGE</p></td>
<td><p>LONGBINARY, GENERAL, OLEOBJECT</p></td>
<td><p>IMAGE</p></td>
</tr>
<tr class="odd">
<td><p>Non pris en charge</p></td>
<td><p>TEXT (voir Remarques)</p></td>
<td><p>LONGTEXT, LONGCHAR, MEMO, NOTE, NTEXT (voir Remarques)</p></td>
<td><p>TEXT</p></td>
</tr>
<tr class="even">
<td><p>CHARACTER, CHARACTER VARYING, NATIONAL CHARACTER, NATIONAL CHARACTER VARYING</p></td>
<td><p>CHAR (voir Remarques)</p></td>
<td><p>TEXT(n), ALPHANUMERIC, CHARACTER, STRING, VARCHAR, CHARACTER VARYING, NCHAR, NATIONAL CHARACTER, NATIONAL CHAR, NATIONAL CHARACTER VARYING, NATIONAL CHAR VARYING (voir Remarques)</p></td>
<td><p>CHAR, VARCHAR, NCHAR, NVARCHAR</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> - Le type de données BIT ANSI SQL ne correspond pas au type de données BIT Microsoft Access SQL. En revanche, il correspond au type de données BINARY. Il n'existe aucun équivalent ANSI SQL pour le type de données BIT Microsoft Access SQL.
> - TIMESTAMP n'est plus reconnu comme synonyme de DATETIME.
> - NUMERIC n'est plus reconnu comme synonyme de FLOAT ou DOUBLE. NUMERIC est désormais utilisé comme synonyme de DECIMAL.
> - Un champ LONGTEXT est toujours stocké dans le format de représentation Unicode.
> - Si le nom du type de données TEXT est utilisé sans que la longueur facultative soit spécifiée, par exemple TEXT(25), un champ LONGTEXT est créé. Des [instructions CREATE TABLE](create-table-statement-microsoft-access-sql.md) sont alors créées pour produire des types de données cohérents avec Microsoft SQL Server.
> - Un champ CHAR est toujours stocké dans le format de représentation Unicode qui est l'équivalent du type de données NATIONAL CHAR ANSI SQL.
> - Si le nom du type de données TEXT est utilisé et si la longueur facultative est spécifiée, par exemple TEXT(25), le type de données du champ est équivalent au type de données CHAR. Ceci permet d'assurer la compatibilité avec les anciennes versions de la plupart des applications Microsoft Jet et d'aligner le type de données TEXT (sans spécification de longueur) avec Microsoft SQL Server.


