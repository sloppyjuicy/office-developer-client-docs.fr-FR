---
title: Détermination du mode Édition
TOCTitle: Determining Edit mode
ms:assetid: 45e21fa7-94e8-3449-e062-09cbcf15cba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249215(v=office.15)
ms:contentKeyID: 48544563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 260cb7b9d2aeed3e230da87fe7bf2571e121cfc1
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63626681"
---
# <a name="determining-edit-mode"></a>Détermination du mode Édition


**S’applique à** : Access 2013, Office 2013

ADO gère une mémoire tampon de modification associée à l'enregistrement actif. La propriété **EditMode** indique si cette mémoire tampon a été modifiée ou si un nouvel enregistrement a été créé. Utilisez **EditMode** pour déterminer l'état de modification de l'enregistrement actif. Vous pouvez vérifier s'il existe des modifications en attente en cas d'interruption d'un processus de modification et déterminer si vous avez besoin d'utiliser la méthode **Update** ou **CancelUpdate**.

**EditMode** retourne une des constantes **EditModeEnum**, telles qu'elles sont répertoriées dans le tableau suivant.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adEditNone</strong></p></td>
<td><p>Indique qu'aucune opération d'édition n'est en cours.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditInProgress</strong></p></td>
<td><p>Indique que les données de l'enregistrement en cours ont été modifiées, mais pas enregistrées.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEditAdd</strong></p></td>
<td><p>Indique que la méthode <strong>AddNew</strong> a été appelée et que l'enregistrement actif dans le tampon de copie est un nouvel enregistrement qui n'a pas été enregistré dans la base de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>adEditDelete</strong></p></td>
<td><p>Indique que l'enregistrement actif a été supprimé.</p></td>
</tr>
</tbody>
</table>


**EditMode** peut retourner une valeur valide seulement s'il existe un enregistrement actif. **EditMode** retourne une erreur si la propriété **BOF** ou **EOF** a la valeur **True** ou si l'enregistrement actif a été supprimé.

