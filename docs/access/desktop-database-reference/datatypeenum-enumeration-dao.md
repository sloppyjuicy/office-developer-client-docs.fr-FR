---
title: DataTypeEnum, énumération (DAO)
TOCTitle: DataTypeEnum Enumeration
ms:assetid: 59ead483-52fc-53cd-02e6-084814f961ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194420(v=office.15)
ms:contentKeyID: 48545028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: d3e84e6f68ba7c28c5407f935ea93ca6242b116a
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62465308"
---
# <a name="datatypeenum-enumeration-dao"></a>DataTypeEnum, énumération (DAO)


**S’applique à** : Access 2013, Office 2013

Spécifie le type des données opérationnelles d'un objet.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAttachment</p></td>
<td><p>101</p></td>
<td><p>Type de données Pièce jointe</p></td>
</tr>
<tr class="even">
<td><p>dbBigInt</p></td>
<td><p>16</p></td>
<td><p>Type de données Entier très grand</p></td>
</tr>
<tr class="odd">
<td><p>dbBinary</p></td>
<td><p>9 </p></td>
<td><p>Type de données Binaire</p></td>
</tr>
<tr class="even">
<td><p>dbBoolean</p></td>
<td><p>1</p></td>
<td><p>Type de données Booléen (Vrai/faux)</p></td>
</tr>
<tr class="odd">
<td><p>dbByte</p></td>
<td><p>2</p></td>
<td><p>Type de données Octet (8 bits) data</p></td>
</tr>
<tr class="even">
<td><p>dbChar</p></td>
<td><p>18 </p></td>
<td><p>Type de données Texte (largeur fixe)</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexByte</p></td>
<td><p>102</p></td>
<td><p>Type de données à valeurs multiples Octet</p></td>
</tr>
<tr class="even">
<td><p>dbComplexDecimal</p></td>
<td><p>108</p></td>
<td><p>Type de données à valeurs multiples Décimal</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexDouble</p></td>
<td><p>106</p></td>
<td><p>Type de données à valeurs multiples Virgule flottante double précision</p></td>
</tr>
<tr class="even">
<td><p>dbComplexGUID</p></td>
<td><p>107</p></td>
<td><p>Type de données à valeurs multiples GUID</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexInteger</p></td>
<td><p>103</p></td>
<td><p>Type de données à valeurs multiples Entier</p></td>
</tr>
<tr class="even">
<td><p>dbComplexLong</p></td>
<td><p>104</p></td>
<td><p>Type de données à valeurs multiples Entier long</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexSingle</p></td>
<td><p>105</p></td>
<td><p>Type de données à valeurs multiples Virgule flottante simple précision</p></td>
</tr>
<tr class="even">
<td><p>dbComplexText</p></td>
<td><p>109</p></td>
<td><p>Type de données à valeurs multiples Texte (largeur variable)</p></td>
</tr>
<tr class="odd">
<td><p>dbCurrency</p></td>
<td><p>5</p></td>
<td><p>Type de données Monétaire</p></td>
</tr>
<tr class="even">
<td><p>dbDate</p></td>
<td><p>8 </p></td>
<td><p>Données de valeurs de date</p></td>
</tr>
<tr class="odd">
<td><p>dbDecimal</p></td>
<td><p>20</p></td>
<td><p>Type de données Décimal (ODBCDirect uniquement)</p><p><strong>REMARQUE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Access.</p>
</td>
</tr>
<tr class="even">
<td><p>dbDouble</p></td>
<td><p>7 </p></td>
<td><p>Type de données Virgule flottante double précision</p></td>
</tr>
<tr class="odd">
<td><p>dbFloat</p></td>
<td><p> 21</p></td>
<td><p>Type de données Virgule flottante (ODBCDirect uniquement)</p>



</td>
</tr>
<tr class="even">
<td><p>dbGUID</p></td>
<td><p>15 </p></td>
<td><p>Type de données GUID</p></td>
</tr>
<tr class="odd">
<td><p>dbInteger</p></td>
<td><p>3</p></td>
<td><p>Type de données Entier</p></td>
</tr>
<tr class="even">
<td><p>dbLong</p></td>
<td><p>4</p></td>
<td><p>Type de données Entier long</p></td>
</tr>
<tr class="odd">
<td><p>dbLongBinary</p></td>
<td><p>11</p></td>
<td><p>Type de données Binaire (image bitmap)</p></td>
</tr>
<tr class="even">
<td><p>dbMemo</p></td>
<td><p>12 </p></td>
<td><p>Type de données Mémo (texte étendu)</p></td>
</tr>
<tr class="odd">
<td><p>dbNumeric</p></td>
<td><p>19</p></td>
<td><p>Type de données Numérique (ODBCDirect uniquement)</p>



</td>
</tr>
<tr class="even">
<td><p>dbSingle</p></td>
<td><p>6 </p></td>
<td><p>Type de données Virgule flottante simple précision</p></td>
</tr>
<tr class="odd">
<td><p>dbText</p></td>
<td><p>10</p></td>
<td><p>Type de données Texte (largeur variable)</p></td>
</tr>
<tr class="even">
<td><p>dbTime</p></td>
<td><p>22</p></td>
<td><p>Données au format de l'heure (ODBCDirect uniquement)</p>



</td>
</tr>
<tr class="odd">
<td><p>dbTimeStamp</p></td>
<td><p>23</p></td>
<td><p>Données au format de la date et de l'heure (ODBCDirect uniquement)</p>



</td>
</tr>
<tr class="even">
<td><p>dbVarBinary</p></td>
<td><p>17 </p></td>
<td><p>Type de données Binaire à longueur variable (ODBCDirect uniquement)</p>



</td>
</tr>
</tbody>
</table>

