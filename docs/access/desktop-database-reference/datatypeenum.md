---
title: DataTypeEnum (référence de base de données du bureau Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703964"
---
# <a name="datatypeenum"></a>DataTypeEnum

**S’applique à**: Access 2013, Office 2013

Spécifie le type de données d’un [Champ](field-object-ado.md), d’un [Paramètre](parameter-object-ado.md) ou d’une [Propriété](property-object-ado.md). L’indicateur de type OLE DB correspondant est montré entre parenthèses dans la colonne Description du tableau suivant. Pour plus d’informations sur les types de données OLE DB, consultez le chapitre 13 et l’annexe A du manuel *OLE DB Programmer’s Reference*.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>AdArray<br />
</strong>(Ne s’applique pas à ADOX.)</p></td>
<td><p>0 x 2000</p></td>
<td><p>Une valeur d'indicateur, toujours combinée à une autre constante de type de données, indiquant un tableau de cet autre type de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p>Indique un nombre entier signé de 8 octets (DBTYPE_I8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p>Indique une valeur binaire (DBTYPE_BYTES).</p></td>
</tr>
<tr class="even">
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p>Indique une valeur de type Booléen (DBTYPE_BOOL).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBSTR</strong></p></td>
<td><p>8</p></td>
<td><p>Indique une chaîne de caractères terminée par un caractère Null (Unicode) (DBTYPE_BSTR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adChapter</strong></p></td>
<td><p>136</p></td>
<td><p>Indique une valeur de chapitre de 4 octets qui identifie les lignes dans un jeu de lignes enfant (DBTYPE_HCHAPTER).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>Indique une valeur de chaîne (DBTYPE_STR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adCurrency</strong></p></td>
<td><p>6</p></td>
<td><p>Indique une valeur monétaire (DBTYPE_CY). Il s'agit d'un nombre à virgule fixe à 4 chiffres à droite de la virgule décimale. Il est stocké dans un nombre entier signé de 8 octets sur une échelle de 10 000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDate</strong></p></td>
<td><p>7</p></td>
<td><p>Indique une valeur de date (DBTYPE_DATE). Une date est stockée en tant que nombre double, la partie entière étant le nombre de jours depuis le 30 décembre 1899, la partie décimale représentant la fraction d'un jour.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p>Indique une valeur de date (aaaammjj) (DBTYPE_DBDATE).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p>Indique une valeur d'heure (hhmmss) (DBTYPE_DBTIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBTimeStamp</strong></p></td>
<td><p>135</p></td>
<td><p>Indique un horodatage complet (aaaaammjjhhmmss, plus une fraction en milliardièmes) (DBTYPE_DBTIMESTAMP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p>Indique une valeur numérique exacte avec une précision et une échelle fixes (DBTYPE_DECIMAL).</p></td>
</tr>
<tr class="even">
<td><p><strong>longueur fixe</strong></p></td>
<td><p>5</p></td>
<td><p>Indique une valeur à virgule flottante en double précision (DBTYPE_R8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEmpty</strong></p></td>
<td><p>0</p></td>
<td><p>Ne spécifie aucune valeur (DBTYPE_EMPTY).</p></td>
</tr>
<tr class="even">
<td><p><strong>adError</strong></p></td>
<td><p>10</p></td>
<td><p>Indique un code d'erreur à 32 bits (DBTYPE_ERROR).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFileTime</strong></p></td>
<td><p>64</p></td>
<td><p>Indique une valeur 64 bits représentant le nombre d'intervalles de 100 nanosecondes depuis le 1er janvier 1601 (DBTYPE_FILETIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adGUID</strong></p></td>
<td><p>72</p></td>
<td><p>Indique un identificateur universel unique (GUID) (DBTYPE_GUID).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIDispatch</strong></p></td>
<td><p>9</p></td>
<td><p>Indique un pointeur vers une interface <strong>IDispatch</strong> sur un objet COM (DBTYPE_IDISPATCH).
</p><p><strong>Remarque</strong>: ce type de données n’est actuellement pas pris en charge par ADO. L’utilisation peut entraîner des résultats imprévisibles.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>tous les types</strong></p></td>
<td><p>3</p></td>
<td><p>Indique un nombre entier signé de 4 octets (DBTYPE_I4).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIUnknown</strong></p></td>
<td><p>13</p></td>
<td><p>Indique un pointeur vers une interface <strong>IUnknown</strong> sur un objet COM (DBTYPE_IUNKNOWN).
</p><p><strong>Remarque</strong>: ce type de données n’est actuellement pas pris en charge par ADO. L’utilisation peut entraîner des résultats imprévisibles.
</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>Indique une valeur binaire longue.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>Indique une valeur de chaîne longue.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>Indique une valeur de chaîne longue terminée par un caractère Null (Unicode).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p>Indique une valeur numérique exacte avec une précision et une échelle fixes (DBTYPE_NUMERIC).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropVariant</strong></p></td>
<td><p>138</p></td>
<td><p>Indique un PROPVARIANT d'automatisation (DBTYPE_PROP_VARIANT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSingle</strong></p></td>
<td><p>4</p></td>
<td><p>Indique une valeur à virgule flottante en simple précision (DBTYPE_R4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p>Indique un nombre entier signé de 2 octets (DBTYPE_I2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p>Indique un nombre entier signé de 1 octet (DBTYPE_I1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p>Indique un nombre entier non signé de 8 octets (DBTYPE_UI8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p>Indique un nombre entier non signé de 8 octets (DBTYPE_UI4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18</p></td>
<td><p>Indique un nombre entier non signé de 2 octets (DBTYPE_UI2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17</p></td>
<td><p>Indique un nombre entier non signé de 1 octet (DBTYPE_UI1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUserDefined</strong></p></td>
<td><p>132</p></td>
<td><p>Indique une variable définie par l'utilisateur (DBTYPE_UDT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p>Indique une valeur binaire (objet <strong>Parameter</strong> uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p>Indique une valeur de chaîne.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVariant</strong></p></td>
<td><p>12</p></td>
<td><p>Indique un objet <strong>Variant</strong> d'automatisation (DBTYPE_VARIANT).
</p><p><strong>Remarque</strong>: ce type de données n’est actuellement pas pris en charge par ADO. L’utilisation peut entraîner des résultats imprévisibles.</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarNumeric</strong></p></td>
<td><p>139</p></td>
<td><p>Indique une valeur numérique (objet <strong>Parameter</strong> uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>Indique une chaîne de caractères terminée par un caractère Null (Unicode).</p></td>
</tr>
<tr class="even">
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p>Indique une chaîne de caractères terminée par un caractère Null (Unicode) (DBTYPE_WSTR).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.DataType.ARRAY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.BIGINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.BINARY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.BOOLEAN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.BSTR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.CHAPTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.CHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.CURRENCY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DATE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DBDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DBTIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DBTIMESTAMP</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DECIMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DOUBLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.EMPTY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.ERROR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.FILETIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.GUID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.IDISPATCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.IUNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.LONGVARBINARY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.LONGVARCHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.LONGVARWCHAR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.NUMERIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.PROPVARIANT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.SINGLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.SMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.TINYINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.UNSIGNEDBIGINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.UNSIGNEDINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.UNSIGNEDSMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.UNSIGNEDTINYINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.USERDEFINED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.VARCHAR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARIANT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.VARNUMERIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARWCHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.WCHAR</p></td>
</tr>
</tbody>
</table>

