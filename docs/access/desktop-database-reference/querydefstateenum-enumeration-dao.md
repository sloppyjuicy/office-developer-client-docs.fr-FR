---
title: QueryDefStateEnum, énumération (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303317"
---
# <a name="querydefstateenum-enumeration-dao"></a>QueryDefStateEnum, énumération (DAO)


**S’applique à** : Access 2013, Office 2013

Cette énumération est utilisée avec la propriété **Prepare** afin de spécifier la méthode utilisée pour définir la préparation d'une requête.

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
<td><p>dbQPrepare</p></td>
<td><p>0,1</p></td>
<td><p>(Valeur par défaut) L'instruction est préparée (l'API ODBC SQLPrepare est appelée).</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>n°2</p></td>
<td><p>L'instruction n'est pas préparée (l'API ODBC SQLExecDirect est appelée).</p></td>
</tr>
</tbody>
</table>

