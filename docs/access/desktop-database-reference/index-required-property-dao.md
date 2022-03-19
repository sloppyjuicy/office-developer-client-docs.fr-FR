---
title: Index.Required, propriété (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: ee5022635fcc6308471daebaa066cd7742e1836a
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628655"
---
# <a name="indexrequired-property-dao"></a>Index.Required, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique si un objet **[Field](field-object-dao.md)** requiert une valeur non Null.

## <a name="syntax"></a>Syntaxe

*.* Obligatoire

*expression* Variable qui représente un objet **Index** .

## <a name="remarks"></a>Remarques

> [!NOTE]
> [!REMARQUE] Lorsque vous définissez cette propriété pour un objet **Index** ou **Field**, définissez-la pour l'objet **Field**. La validité du paramètre de propriété d'un objet **Field** est vérifiée avant celle d'un objet **Index**.

La disponibilité de la propriété **Required** dépend de l'objet contenant la collection [Fields](fields-collection-dao.md), comme illustré dans le tableau suivant.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Si la collection Fields appartient à un</p></th>
<th><p>Alors Required est</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>objet <strong>Index</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p>objet <strong>Relation</strong></p></td>
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p>objet <strong>TableDef</strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
</tbody>
</table>

