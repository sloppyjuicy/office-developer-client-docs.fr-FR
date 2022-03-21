---
title: SynchronizeTypeEnum, éumération (DAO)
TOCTitle: SynchronizeTypeEnum Enumeration
ms:assetid: f9546171-283d-e9bd-5178-41bd4f41c9a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837004(v=office.15)
ms:contentKeyID: 48548812
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a7d6f910f03dc04495b6c40e852c849aa33ee69
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630482"
---
# <a name="synchronizetypeenum-enumeration-dao"></a>SynchronizeTypeEnum, éumération (DAO)


**S’applique à** : Access 2013, Office 2013

Cette énumération est utilisée avec la méthode **Synchronize** pour déterminer le type de synchronisation à appliquer à deux réplicas.

<table>
<colgroup>
<col />
<col />
<col />
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
<td><p>dbRepExportChanges</p></td>
<td><p>1</p></td>
<td><p>Envoie les modifications de la base de données active vers la base de données cible.</p></td>
</tr>
<tr class="even">
<td><p>dbRepImpExpChanges</p></td>
<td><p>4</p></td>
<td><p>Envoie et reçoit les données dans le cadre d'un transfert bidirectionnel.</p></td>
</tr>
<tr class="odd">
<td><p>dbRepImportChanges</p></td>
<td><p>2</p></td>
<td><p>Reçoit les modifications de la base de données cible.</p></td>
</tr>
<tr class="even">
<td><p>dbRepSyncInternet</p></td>
<td><p>16</p></td>
<td><p>Envoie et reçoit les données dans le cadre d'un transfert bidirectionnel.</p></td>
</tr>
</tbody>
</table>

