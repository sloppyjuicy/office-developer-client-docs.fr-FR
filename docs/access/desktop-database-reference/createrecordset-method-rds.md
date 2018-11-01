---
title: CreateRecordset, méthode (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d975faf45cf6a16bdae9f800084ebbbbaec3127d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868531"
---
# <a name="createrecordset-method-rds"></a>CreateRecordset, méthode (RDS)


**S’applique à**: Access 2013, Office 2013


Crée un objet [Recordset](recordset-object-ado.md) vide et déconnecté.

## <a name="syntax"></a>Syntaxe

*objet*. CreateRecordset (*ColumnInfos*)

## <a name="parameters"></a>Paramètres

  - *Object*

  - Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) ou [RDS.DataControl](datacontrol-object-rds.md).

  - *ColumnsInfos*

  - Tableau de type **Variant** qui contient des attributs et définit chaque colonne de l'objet **Recordset** créé. Chaque définition de colonne contient un tableau de quatre attributs obligatoires et un attribut facultatif. Le jeu de tableaux de colonnes est ensuite regroupé dans un tableau qui définit l'objet **Recordset**.
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Attribut</p></th>
    <th><p>Description</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Name</p></td>
    <td><p>Nom de l'en-tête de colonne.</p></td>
    </tr>
    <tr class="even">
    <td><p>Type</p></td>
    <td><p>Entier du type de données.</p></td>
    </tr>
    <tr class="odd">
    <td><p>Size</p></td>
    <td><p>Entier de la largeur en caractères, quel que soit le type de données.</p></td>
    </tr>
    <tr class="even">
    <td><p>Nullability</p></td>
    <td><p>Valeur de type Boolean.</p></td>
    </tr>
    <tr class="odd">
    <td><p>Scale (Échelle)<br />
(Facultatif)</p></td>
    <td><p>Cet attribut facultatif définit l'échelle des champs numériques. Si cette valeur n'est pas spécifiée, les valeurs numériques sont tronquées à une échelle de trois. La précision n'est pas affectée, mais le nombre de chiffres après la virgule est tronqué après trois.</p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a>Notes

L'objet métier côté serveur peut remplir l'objet **Recordset** résultant avec des données provenant d'un fournisseur de données non OLE DB, tel qu'un fichier du système d'exploitation contenant les cours des actions.

Le tableau suivant répertorie les valeurs de l'énumération [DataTypeEnum](datatypeenum.md) prises en charge par la méthode **CreateRecordset**. Le nombre indiqué correspond au numéro de référence utilisé pour définir des champs.

Chaque type de données est de longueur fixe ou variable. Les types de longueur fixe doivent être définis par la taille –1, parce que la taille est prédéterminée et que la définition de la taille est toujours obligatoire. Les types de données de longueur variable permettent d'obtenir une taille situé entre 1 et 32767.

Pour certains types de données variables, il est possible de forcer une conversion du type dans le type indiqué dans la colonne Substitution. Vous ne voyez les substitutions qu'une fois l'objet **Recordset** créé et rempli. Vous pouvez alors vérifier le type de données réel, le cas échéant.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Longueur</p></th>
<th><p>Constante</p></th>
<th><p>Nombre</p></th>
<th><p>Substitution</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>tous les types</strong></p></td>
<td><p>3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adSingle</strong></p></td>
<td><p>4</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>longueur fixe</strong></p></td>
<td><p>5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adCurrency</strong></p></td>
<td><p>6</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adError</strong></p></td>
<td><p>10</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adGuid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adDate</strong></p></td>
<td><p>7</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixe</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixe</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adBSTR</strong></p></td>
<td><p>8</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Variable</p></td>
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Variable</p></td>
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>

