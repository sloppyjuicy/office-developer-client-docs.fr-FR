---
title: CursorLocationEnum (référence de base de données du bureau Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470451"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie l'emplacement du service de curseur.

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
<td><p>Par défaut. Utilise des curseurs de type données ou pilote. Ces curseurs sont parfois très souples et acceptent plus facilement les modifications apportées aux données sources. Toutefois, certaines fonctions du <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (comme les objets <a href="recordset-object-ado.md">Recordset</a> dissocciés) ne peuvent être simulés avec les curseurs de type serveur ; ces fonctions seront indisponibles avec ce paramètre.</p></td>
</tr>
</tbody>
</table>


**Équivalent ADO/WFC**

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

