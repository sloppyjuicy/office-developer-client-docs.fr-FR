---
title: Fonctions scalaires ODBC
TOCTitle: ODBC scalar functions
ms:assetid: dc1096bf-8241-036a-14c6-b19afae45454
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835353(v=office.15)
ms:contentKeyID: 48548120
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277473
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 33443fda474b3785d34d457719e49f5e358bb254
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288510"
---
# <a name="odbc-scalar-functions"></a>Fonctions scalaires ODBC

**S’applique à** : Access 2013, Office 2013

Microsoft Access SQL prend en charge l'utilisation de la syntaxe définie par ODBC pour les fonctions scalaires. 

Par exemple, la requête `SELECT DAILYCLOSE, DAILYCHANGE FROM DAILYQUOTE WHERE {fn ABS(DAILYCHANGE)} > 5` renvoie toutes les lignes où la valeur absolue de la modification du prix d'une action était supérieure à cinq.

Un sous-ensemble des fonctions scalaires ODBC est pris en charge. La tableau suivant répertorie les fonctions prises en charge.

Pour une description des arguments et une explication complète de la syntaxe d'échappement permettant d'inclure des fonctions dans une instruction SQL, consultez la documentation ODBC.

## <a name="string-functions"></a>Fonctions de chaîne

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ASCII</p></td>
<td><p>LAPS</p></td>
<td><p>RTRIM</p></td>
</tr>
<tr class="even">
<td><p>ÉCHELLE</p></td>
<td><p>REPÉRER</p></td>
<td><p>ESPACE</p></td>
</tr>
<tr class="odd">
<td><p>CONCAT</p></td>
<td><p>LTRIM</p></td>
<td><p>SOUS-chaîne</p></td>
</tr>
<tr class="even">
<td><p>LCASE</p></td>
<td><p>Oui</p></td>
<td><p>UCASE</p></td>
</tr>
<tr class="odd">
<td><p>RENSEIGNÉ</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="numeric-functions"></a>Fonctions numériques

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>ABS</p></td>
<td><p>CHAUSSÉE</p></td>
<td><p>SINE</p></td>
</tr>
<tr class="even">
<td><p>ATAN</p></td>
<td><p>ROUVRIR</p></td>
<td><p>COMPLEXE</p></td>
</tr>
<tr class="odd">
<td><p>ENCASTRE</p></td>
<td><p>CONSOMMATION</p></td>
<td><p>TAN</p></td>
</tr>
<tr class="even">
<td><p>SINU</p></td>
<td><p>VÉRIFICATIONS</p></td>
<td><p>MSSQL</p></td>
</tr>
<tr class="odd">
<td><p>PRÉVU</p></td>
<td><p>INSCRIV</p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


## <a name="time--date-functions"></a>Fonctions de date et d'heure &

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>CAILLÉ</p></td>
<td><p>DAYOFYEAR</p></td>
<td><p>SEMESTRIELLE</p></td>
</tr>
<tr class="even">
<td><p>CURTIME</p></td>
<td><p>AUTRE</p></td>
<td><p>MENSUEL</p></td>
</tr>
<tr class="odd">
<td><p>F1</p></td>
<td><p>H/24</p></td>
<td><p>TRIMESTRE</p></td>
</tr>
<tr class="even">
<td><p>DAYOFMONTH</p></td>
<td><p>PRÉCÉDENTE</p></td>
<td><p>MONTHNAME</p></td>
</tr>
<tr class="odd">
<td><p>DAYOFWEEK</p></td>
<td><p>SECONDE</p></td>
<td><p>DAYNAME</p></td>
</tr>
</tbody>
</table>


## <a name="data-type-conversion"></a>Conversion de type de données

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>REMPLACER</p></td>
<td><p>Les littéraux de chaîne peuvent être convertis dans les types de données suivants : SQL_FLOAT, SQL_DOUBLE, SQL_NUMERIC, SQL_INTEGER, SQL_REAL, SQL_SMALLINT, SQL_VARCHAR et SQL_DATETIME.</p></td>
</tr>
</tbody>
</table>

