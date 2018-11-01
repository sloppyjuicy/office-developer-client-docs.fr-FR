---
title: QueryDefStateEnum Enumeration (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b368079aeb668c9ae72e3955f55159ab2c72a53e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882566"
---
# <a name="querydefstateenum-enumeration-dao"></a>QueryDefStateEnum Enumeration (DAO)


**S’applique à**: Access 2013, Office 2013

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
<td><p>1</p></td>
<td><p>(Valeur par défaut) L'instruction est préparée (l'API ODBC SQLPrepare est appelée).</p></td>
</tr>
<tr class="even">
<td><p>dbQUnprepare</p></td>
<td><p>2</p></td>
<td><p>L'instruction n'est pas préparée (l'API ODBC SQLExecDirect est appelée).</p></td>
</tr>
</tbody>
</table>

