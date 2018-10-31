---
title: CursorLocationEnum (référence de base de données du bureau Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863628"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**S’applique à**: Access 2013 | Office 2013

Spécifie l'emplacement du service de curseur.

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
<td><p><strong>adUseClient</strong></p></td>
<td><p>3</p></td>
<td><p>Utilise les curseurs côté client fournis par une bibliothèque de curseurs local. Services de curseur locaux souvent permettra de nombreuses fonctionnalités qui pilote curseurs ne peuvent pas, afin que ce paramètre peut fournir un avantage en ce qui concerne les fonctionnalités que vous souhaitez activer. Pour assurer la compatibilité descendante, le synonyme <strong>adUseClientBatch</strong> est également pris en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>N'utilise pas les services de curseur. (Cette constante est obsolète et n'est présente qu'à des fins de compatibilité ascendante.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Par défaut. Utilise les curseurs pilote ou fournisseur de données. Ces curseurs sont parfois très souples et autoriser plus facilement les modifications apportées à la source de données. Cependant, certaines fonctionnalités du <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Service de curseur Microsoft pour OLE DB</a> (telles que les objets <a href="recordset-object-ado.md">Recordset</a> dissociées) ne peut pas être simuler avec les curseurs côté serveur, et ces fonctionnalités ne seront pas disponibles avec ce paramètre.</p></td>
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
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

