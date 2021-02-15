---
title: ActionEnum (référence de base de données de bureau Access)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280655"
---
# <a name="actionenum"></a>ActionEnum

**S’applique à** : Access 2013, Office 2013

Indique le type d’action à effectuer lorsque la méthode [SetPermissions](setpermissions-method-adox.md) est appelée.

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
<td><p><strong>adAccessDeny</strong></p></td>
<td><p>3 </p></td>
<td><p>Les autorisations spécifiées seront refusées au groupe ou à l'utilisateur.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessGrant</strong></p></td>
<td><p>1 </p></td>
<td><p>Le groupe ou l'utilisateur disposera au moins des autorisations demandées.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAccessRevoke</strong></p></td>
<td><p>4 </p></td>
<td><p>Tous les droits d'accès explicites que le groupe ou l'utilisateur possède seront révoqués.</p></td>
</tr>
<tr class="even">
<td><p><strong>adAccessSet</strong></p></td>
<td><p>2 </p></td>
<td><p>Le groupe ou l'utilisateur disposera exactement des autorisations demandées.</p></td>
</tr>
</tbody>
</table>

