---
title: Résumé du modèle objet RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a929815a9c125505ff05f87da1bfea3a6892bc81
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628670"
---
# <a name="rds-object-model-summary"></a>Résumé du modèle objet RDS


**S’applique à** : Access 2013, Office 2013

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">RDS. DataSpace</a></p></td>
<td><p>Cet objet contient une méthode permettant d’obtenir un proxy serveur qui peut être le proxy par défaut ou un programme serveur personnalisé (objet métier). Le programme serveur peut être appelé sur Internet, un intranet, un réseau local ou être une bibliothèque de liens dynamiques locale.</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></p></td>
<td><p>Cet objet représente le programme serveur par défaut. Il met en œuvre le comportement par défaut d'extraction et de mise à jour des données RDS.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">RDS. DataControl</a></p></td>
<td><p>Cet objet est capable d'appeler automatiquement les objets <strong>RDS.DataSpace</strong> et <strong>RDSServer.DataFactory</strong>. Utilisez-le pour appeler le comportement par défaut d'extraction ou de mise à jour des données RDS. Cet objet permet également aux contrôles visuels d'accéder à l'objet <strong>Recordset</strong> retourné.</p></td>
</tr>
</tbody>
</table>

