---
title: UpdateTypeEnum Enumeration (DAO)
TOCTitle: UpdateTypeEnum Enumeration
ms:assetid: 7ac38bae-27fc-f3d0-5b75-569bce547954
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196186(v=office.15)
ms:contentKeyID: 48545800
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd2ef7888f511b3f1577ec5fe60ef0ef7dda614a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873445"
---
# <a name="updatetypeenum-enumeration-dao"></a>UpdateTypeEnum Enumeration (DAO)


**S’applique à**: Access 2013, Office 2013

Cette énumération est utilisée avec la méthode **Update** pour spécifier les mises à jour à écrire sur le disque.

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
<td><p>dbUpdateBatch ne</p></td>
<td><p>4</p></td>
<td><p>Toutes les modifications en attente dans le cache de mise à jour sont écrites sur le disque.</p></td>
</tr>
<tr class="even">
<td><p>dbUpdateCurrentRecord</p></td>
<td><p>2</p></td>
<td><p>Seules les modifications en attente de l'enregistrement actif sont écrites sur le disque.</p></td>
</tr>
<tr class="odd">
<td><p>valeurs de dbUpdateRegular</p></td>
<td><p>1</p></td>
<td><p>(Valeur par défaut) Les modifications en attente ne sont pas mises en cache. Elles sont écrites immédiatement sur le disque.</p></td>
</tr>
</tbody>
</table>

