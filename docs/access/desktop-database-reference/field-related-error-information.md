---
title: Informations sur les erreurs relatives aux champs
TOCTitle: Field-related error information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e853c45e4ee0de9a958ccc791bac3afcd305a23
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943562"
---
# <a name="field-related-error-information"></a>Informations sur les erreurs relatives aux champs


**S’applique à**: Access 2013, Office 2013

Si une erreur est directement liée à un champ  par exemple, si les données sont manquantes ou si le type du champ est incorrect  vous pouvez obtenir plus d'informations sur la cause du problème en examinant la propriété **Status** de l'objet **Field**. Cette propriété a été améliorée afin de fournir des informations spécifiques relatives au problème. Ainsi, par exemple, lorsqu'une invocation de **UpdateBatch** échoue, la cause du problème peut être déterminée en examinant la propriété **Status** des **champs** de chaque enregistrement affecté. La propriété contient une des valeurs dans la constante **FieldStatusEnum**. Le tableau suivant contient les valeurs qui présentent un intérêt lorsqu'une erreur survient.

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
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Indique que le champ ne peut pas être extrait ni stocké sans perte de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Indique que les données renvoyées par le fournisseur ont dépassé le type de données du champ.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Indique que la valeur par défaut du champ a été utilisée lors de la définition des données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Indique que ce champ a été ignoré lors de la définition des valeurs de données dans la source. Aucune valeur n'est définie par le fournisseur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Indique que le champ ne peut pas être modifié car il s'agit d'une entité calculée ou dérivée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Indique que le fournisseur a renvoyé une valeur NULL.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Indique que le fournisseur ne parvient pas à obtenir suffisamment d'espace de stockage pour réaliser un déplacement ou une copie.</p></td>
</tr>
</tbody>
</table>

