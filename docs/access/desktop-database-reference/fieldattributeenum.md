---
title: FieldAttributeEnum (référence de base de données du bureau Access)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cbfc4a45b3a85704fe8c9e6a7b984456ac783b35
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864081"
---
# <a name="fieldattributeenum"></a>FieldAttributeEnum

**S’applique à**: Access 2013 | Office 2013

Spécifie un ou plusieurs attributs d'un objet [Field](field-object-ado.md).

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFldCacheDeferred</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Indique que le fournisseur met en mémoire cache les valeurs des champs et que les lectures suivantes sont effectuées depuis la mémoire cache.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldFixed</strong></p></td>
<td><p>0 x 10</p></td>
<td><p>Indique que le champ contient des données de longueur fixe.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsChapter</strong></p></td>
<td><p>0 x 2000</p></td>
<td><p>Indique que le champ contient une valeur de chapitre, qui spécifie un recordset enfant lié à ce champ parent. En général, les champs de chapitre sont utilisés avec le service Data Shaping ou les filtres.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsCollection</strong></p></td>
<td><p>0 x 40000</p></td>
<td><p>Indique que le champ spécifie que la ressource représentée par l'enregistrement est une collection d'autres ressources, comme un dossier, plutôt que comme une ressource simple comme un fichier texte.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsDefaultStream</strong></p></td>
<td><p>0 x 20000</p></td>
<td><p>Indique que le champ contient le flux par défaut pour la ressource représentée par l’objet record. Par exemple, le flux par défaut peut être le contenu HTML d’un dossier racine sur un site Web, qui est automatiquement servi lorsque l’URL racine est spécifié.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldIsNullable</strong></p></td>
<td><p>0 x 20</p></td>
<td><p>Indique que le champ accepte des valeurs nulles.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldIsRowURL</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Indique que le champ contient l'URL qui appelle la ressource à partir de l'emplacement des données représenté par l'enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldLong</strong></p></td>
<td><p>0 x 80</p></td>
<td><p>Indique que le champ est de type binaire long. Indique également que vous pouvez utiliser les méthodes <a href="appendchunk-method-ado.md">AppendChunk</a> et <a href="getchunk-method-ado.md">GetChunk</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldMayBeNull</strong></p></td>
<td><p>0 x 40</p></td>
<td><p>Indique que vous pouvez lire des valeurs nulles à partir du champ.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldMayDefer</strong></p></td>
<td><p>0x2</p></td>
<td><p>Indique que le champ est différé : ses valeurs ne sont pas extraites de la source de données avec l'intégralité de l'enregistrement, mais seulement lors d'un accès explicite de votre part.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldNegativeScale</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Indique que le champ représente une valeur numérique depuis une colonne qui prend en charge les valeurs d’échelle négatives. L’échelle est spécifiée par la propriété <a href="numericscale-property-ado.md">NumericScale</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldRowID</strong></p></td>
<td><p>0 x 100</p></td>
<td><p>Indique que le champ contient un identificateur de lignes persistantes sur lequel il n'est pas possible d'écrire et qui ne possède pas de valeurs significatives, sauf pour l'identification de la ligne (comme un numéro d'enregistrement, un identificateur unique, etc.).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldRowVersion</strong></p></td>
<td><p>0 x 200</p></td>
<td><p>Indique que le champ contient un horodatage (heure ou date) utilisé pour suivre les mises à jour.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUnknownUpdatable</strong></p></td>
<td><p>0 x 8</p></td>
<td><p>Indique que le fournisseur ne peut déterminer si vous pouvez écrire dans le champ.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFldUnspecified</strong></p></td>
<td><p>-1<br />
0xFFFFFFFF</p></td>
<td><p>Indique que le fournisseur ne spécifie pas d'attributs pour le champ.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFldUpdatable</strong></p></td>
<td><p>0 x 4</p></td>
<td><p>Indique que vous pouvez écrire dans le champ.</p></td>
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
<td><p>AdoEnums.FieldAttribute.CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.FIXED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.ISNULLABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.LONG</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.MAYBENULL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.MAYDEFER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.NEGATIVESCALE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.ROWID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.ROWVERSION</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.FieldAttribute.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.FieldAttribute.UPDATABLE</p></td>
</tr>
</tbody>
</table>

