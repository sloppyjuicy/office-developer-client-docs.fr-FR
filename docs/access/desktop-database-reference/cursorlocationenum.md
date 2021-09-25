---
title: CursorLocationEnum (référence de base de données de bureau Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d81a086e2ead45dbc56f5be5f24ba8bf5937f7a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615633"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**S’applique à** : Access 2013, Office 2013

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
<td><p>Utilise des curseurs côté client fournis par une bibliothèque de curseurs locale. Les services de curseur locaux disposent de beaucoup plus de fonctions que les curseurs fournis par les pilotes ; ce paramètre peut donc présenter un avantage pour les fonctions activées. Pour des questions de compatibilité ascendante, le synonyme <strong>adUseClientBatch</strong> est également pris en charge.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>N'utilise pas les services de curseur. (Cette constante est obsolète et n'est présente qu'à des fins de compatibilité ascendante.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Valeur par défaut. Utilise des curseurs de type données ou pilote. Ces curseurs sont parfois très souples et acceptent plus facilement les modifications apportées aux données sources. Toutefois, certaines fonctionnalités du service de curseur Microsoft pour <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">OLE DB</a> (telles que les objets <a href="recordset-object-ado.md">Recordset</a> dissociés) ne peuvent pas être simulées avec des curseurs côté serveur, et ces fonctionnalités ne seront pas disponibles avec ce paramètre.</p></td>
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

