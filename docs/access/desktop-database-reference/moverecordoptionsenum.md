---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4852562fcc755ae0edc8376d0e59d67a1e0affe0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558197"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**S’applique à** : Access 2013, Office 2013

Spécifie le fonctionnement de la méthode [MoveRecord](moverecord-method-ado.md) de l’objet [Record](record-object-ado.md) .

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
<td><p><strong>adMoveUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Par défaut. Effectue l'opération de déplacement par défaut : l'opération échoue si le fichier ou répertoire de destination existe déjà ; elle met alors à jour les liens hypertexte.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Remplace le fichier ou répertoire de destination, même s'il existe déjà.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Modifie le fonctionnement par défaut de la méthode <strong>MoveRecord</strong> en ne mettant pas à jour les liens hypertexte du <strong>Record</strong> source. Le fonctionnement par défaut dépend des capacités du fournisseur. L'opération Move met à jour les liens si le fournisseur en est capable. Si le fournisseur ne peut résoudre les liens ou si cette valeur n'est pas spécifiée, le déplacement réussit même si les liens n'ont pas été mis à jour.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4 </p></td>
<td><p>Demande au fournisseur de simuler le déplacement (à l'aide d'opérations de téléchargement, de chargement et de suppression). Si la tentative de déplacement du <strong>Record</strong> échoue parce que l'URL de destination se trouve sur un autre serveur ou si elle est servie par un autre fournisseur que la source des données, il peut en résulter une latence accrue ou une perte de données, en raison des caractéristiques différentes des fournisseurs.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

