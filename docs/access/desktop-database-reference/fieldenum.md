---
title: FieldEnum (référence de base de données de bureau Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292593"
---
# <a name="fieldenum"></a>FieldEnum

**S’applique à** : Access 2013, Office 2013

Spécifie les champs spéciaux référencés dans une collection [Fields](record-object-ado.md) d'un objet [Record](fields-collection-ado.md).

## <a name="remarks"></a>Remarques

Ces constantes représentent un "raccourci" pour accéder aux champs spéciaux associés à un objet **Record**. Extrayez l’objet [Field](field-object-ado.md) depuis la collection **Fields**, puis obtenez son contenu avec la propriété [Value](value-property-ado.md) de l’objet **Field**.

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
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p>Référence le champ contenant l’objet <a href="stream-object-ado.md">Stream</a> par défaut associé à un <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>Référence le champ contenant la chaîne d’URL absolue du <strong>Record</strong> en cours.</p></td>
</tr>
</tbody>
</table>

