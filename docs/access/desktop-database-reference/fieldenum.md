---
title: FieldEnum (référence de base de données de bureau Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8400379df7016d9d607304d428d2f8deb7ccba3b
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464188"
---
# <a name="fieldenum"></a>FieldEnum

**S’applique à** : Access 2013, Office 2013

Spécifie les champs spéciaux référencés dans une collection [Fields](record-object-ado.md) d'un objet [Record](fields-collection-ado.md).

## <a name="remarks"></a>Remarques

Ces constantes représentent un "raccourci" pour accéder aux champs spéciaux associés à un objet **Record**. Extrayez l’objet [Field](field-object-ado.md) depuis la collection **Fields**, puis obtenez son contenu avec la propriété [Value](value-property-ado.md) de l’objet **Field**.


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

